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
      {
        data: { 
          id: 'nav2_controller',
          label: 'nav2_controller server\n/module_base_controller/odom',
          url: 'https://pramanic.fi/My-Pins/Sick-Robot-SLAM-and-Gmapping'
        },
        position: { x: 400, y: 300 }
      },
      // Add other nodes here following the same pattern
      {
        data: { 
        id: 'Gmapping_map',
        label: 'Gmapping,
        url: 'https://pramanic.fi/My-Pins/Sick-Robot-SLAM-and-Gmapping' 
  },
        position: { x: 100, y: 100 }  // Set coordinates
       },


    ],
    style: [
      {
        selector: 'node',
        style: {
          'label': 'data(label)',
          'text-valign': 'center',
          'text-halign': 'center',
          'font-family': 'Ubuntu Mono, monospace',
          'font-size': 12,
          'color': '#2c3e50',
          'background-color': '#e0e7ff',
          'border-color': '#6366f1',
          'border-width': 2,
          'shape': 'rectangle',
          'padding': 20,
          'text-max-width': '180px',
          'text-wrap': 'wrap',
          'width': 'label',
          'height': 'label',
          'min-width': '100px',
          'min-height': '60px',
          'text-margin-y': 10,
          'text-margin-x': 15
        }
      },
      {
        selector: 'edge',
        style: {
          'width': 2,
          'line-color': '#4f46e5',
          'curve-style': 'straight',
          'target-arrow-shape': 'triangle'
        }
      }
    ],
    layout: { 
      name: 'preset',
      nodeDimensionsIncludeLabels: true  // Critical for text containment
    }
  });

  // Enable pan/zoom
  cy.userPanningEnabled(true);
  cy.userZoomingEnabled(true);

  // Click handler for nodes
  cy.on('tap', 'node', (event) => {
    const node = event.target;
    if(node.data('url')) {
      window.location.href = node.data('url');
    }
  });
</script>