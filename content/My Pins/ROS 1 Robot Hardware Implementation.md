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

<script src="https://cdnjs.cloudflare.com/ajax/libs/cytoscape/3.23.0/cytoscape.min.js"></script>

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
  const cy = cytoscape({
    container: document.getElementById('cy'),
    elements: [
      // Nodes
      { 
        data: { 
          id: 'nav2_planner',
          label: 'nav2_planner_server\n/mobile_base_controller/odom',
          url: '/path/to/nav2_details' 
        },
        position: { x: 200, y: 100 }
      },
      {
        data: {
          id: 'controller',
          label: 'nav2_controller_server\n/local_costmap',
          url: '/path/to/controller_details'
        },
        position: { x: 600, y: 100 }
      },
      // Edges
      { data: { id: 'e1', source: 'nav2_planner', target: 'controller' } }
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
          'color': '#2c3e50',
          'background-color': '#e0e7ff',
          'border-color': '#6366f1',
          'border-width': '2px',
          'shape': 'rectangle',
          'padding': '15px',
          'text-max-width': '200px',
          'text-wrap': 'wrap',
          'min-width': '100px',
          'min-height': '50px'
        }
      },
      {
        selector: 'edge',
        style: {
          'width': 2,
          'line-color': '#4f46e5',
          'curve-style': 'straight',
          'target-arrow-shape': 'triangle',
          'target-arrow-color': '#4f46e5',
          'arrow-scale': 1.5
        }
      },
      {
          node:hover {
               background-color: #c7d2fe;
               cursor: pointer;
         }
      }
      
    ],
    layout: { name: 'preset' }
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

  // Automatically fit nodes to text
  cy.nodes().layout({
    name: 'cola',
    fit: true,
    padding: 30,
    nodeDimensionsIncludeLabels: true
  }).run();
</script>