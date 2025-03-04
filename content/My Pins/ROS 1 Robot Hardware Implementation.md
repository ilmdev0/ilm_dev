---
title: ROS 1 Robot Hardware Implementation
date: false
draft: false
tags: 
publish: true
---

> [!done] ROS 1
> Hardware Implementation Architecture Graph


<div id="cy"></div>

<!-- Load Cytoscape -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/cytoscape/3.23.0/cytoscape.min.js"></script>
<!-- Load Cola.js layout extension -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/cytoscape-cola/2.1.0/cytoscape-cola.min.js"></script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Ubuntu+Mono&display=swap');
  
  #cy {
    width: 100%;
    height: 800px;
    border: 1px solid #444;
    background: #f8f8f8;
  }
</style>

<script>
  function initializeGraph() {
    const container = document.getElementById('cy');
    if (!container) return;

    container.innerHTML = ''; // Clear previous graph instance

    const cy = cytoscape({
      container: container,
      elements: [
        // Nodes
        { 
          data: { 
            id: 'nav2_planner',
            label: 'nav2_planner_server\n/mobile_base_controller/odom',
            url: 'https://pramanic.fi/My-Pins/Sick-Robot-SLAM-and-Gmapping' 
          },
          position: { x: 200, y: 100 }
        },
        {
          data: {
            id: 'controller',
            label: 'nav2_controller_server\n/local_costmap',
            url: 'https://pramanic.fi/My-Pins/Sick-Robot-SLAM-and-Gmapping'
          },
          position: { x: 600, y: 100 }
        },
        {
          data: {
            id: 'gmapping',
            label: 'Gmapping',
            url: 'https://pramanic.fi/My-Pins/Sick-Robot-SLAM-and-Gmapping'
          },
          position: { x: 800, y: 100 }
        },
        {
          data: {
            id: 'slam',
            label: 'slam_tool_box',
            url: 'https://pramanic.fi/My-Pins/Sick-Robot-SLAM-and-Gmapping'
          },
          position: { x: 800, y: 200 }
        },

        // Edges
        { data: { id: 'e1', source: 'nav2_planner', target: 'controller' } },
        { data: { id: 'e2', source: 'controller', target: 'gmapping' } },
        { data: { id: 'e3', source: 'controller', target: 'slam' } }
      ],

      style: [
        {
          selector: 'node',
          style: {
            'label': 'data(label)',
            'text-valign': 'center',
            'text-halign': 'center',
            'font-family': 'Ubuntu Mono, monospace',
            'font-size': '12px',
            'color': '#000000',
            'background-color': '#ffbae1',
            'border-color': '#000000',
            'border-width': '0.5px',
            'shape': 'rectangle',
            'padding': '10px',
            'line-height': '1.2',
            'text-max-width': '180px',
            'text-wrap': 'wrap',
            'width': 'auto',  // Fixed deprecated property
            'height': 'auto', // Fixed deprecated property
            'min-width': '120px',
            'min-height': '120px',
            'text-margin-y': '0px',
            'text-margin-x': '0px'
          }
        },
        {
          selector: 'edge',
          style: {
            'width': 1,
            'line-color': '#f58c8c',
            'curve-style': 'straight',
            'target-arrow-shape': 'triangle',
            'target-arrow-color': '#f55656',
            'arrow-scale': 1
          }
        }
      ],
      layout: { 
        name: 'preset' // Using 'preset' instead of 'cola' by default
      }
    });

    // Enable pan/zoom
    cy.userPanningEnabled(true);
    cy.userZoomingEnabled(true);

    // Click handler for nodes with links
    cy.on('tap', 'node', (event) => {
      const node = event.target;
      const url = node.data('url');
      if(url) {
        window.location.href = url;
      }
    });

    // Use Cola.js layout (Ensure it's loaded first)
    cy.layout({
      name: 'cola',
      fit: true,
      padding: 100
    }).run();
  }

  // Run the function when the page loads
  document.addEventListener('DOMContentLoaded', initializeGraph);

  // Run it again when navigating dynamically (Quartz)
  document.addEventListener('astro:page-load', () => {
    setTimeout(initializeGraph, 100); // Ensure DOM updates before running
  });
</script>
