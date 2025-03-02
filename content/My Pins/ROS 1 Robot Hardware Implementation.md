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

<!-- Include libraries -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/cytoscape/3.23.0/cytoscape.min.js"></script>

<style>
  #cy {
    width: 100%;
    height: 600px;
    border: 1px solid #ccc;
    background: white;
  }
</style>

<script>
  // Initialize graph
  const cy = cytoscape({
    container: document.getElementById('cy'),
    elements: [ /* Nodes and edges */ ],
    style: [ /* Styling */ ],
    layout: { name: 'preset' } // Use predefined positions
  });

  // Enable pan/zoom
  cy.userPanningEnabled(true);
  cy.userZoomingEnabled(true);
</script>

elements: [
  // Nodes
  { data: { id: 'drive', label: 'Drive' }, position: { x: 100, y: 50 } },
  { data: { id: 'int_face', label: 'Int_face_detect' }, position: { x: 300, y: 50 } },
  // Edges
  { data: { id: 'e1', source: 'drive', target: 'int_face' } }
],

// Style

style: [
  {
    selector: 'node',
    style: {
      'label': 'data(label)',
      'background-color': '#6FB1FC',
      'text-valign': 'center',
      'shape': 'rectangle',
      'padding': '10px'
    }
  },
  {
    selector: 'edge',
    style: {
      'width': 2,
      'line-color': '#999',
      'curve-style': 'bezier'
    }
  }
]

// Clickable

cy.on('tap', 'node', (event) => {
  const node = event.target;
  alert(`Clicked: ${node.data('label')}`);
  // Replace with your logic (e.g., open a modal)
});