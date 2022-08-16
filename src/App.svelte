<script lang="ts">
  import Svelvet from 'svelvet';
  import type { Node, Edge } from 'svelvet';

  const initialNodes: Node[] = [
    {
      id: 1,
      position: { x: 200, y: 50 },
      data: { label: 'Input Node' },
      width: 175,
      height: 40,
      bgColor: 'white'
    },
    {
      id: 2,
      position: { x: 25, y: 150 },
      data: { label: 'Option #1' },
      width: 175,
      height: 40,
      bgColor: '#B8FFC6',
      borderColor: 'transparent'
    },
    {
      id: 3,
      position: { x: 375, y: 150 },
      data: { label: 'Option #2' },
      width: 175,
      height: 40,
      bgColor: '#FFB8B8',
      borderColor: 'transparent'
    }
  ];
  const initialEdges: Edge[] = [
    { id: 'e1-2', source: 1, target: 2, label: ' YES ', animate: true },
    { id: 'e2-3', source: 1, target: 3, label: ' NO ', animate: true }
  ];

// Event Handler for New Node Button
  const newNodeHandler = (e) => {

  }
</script>

<Svelvet nodes={initialNodes} edges={initialEdges} background />

<!-- Create New Node Button -->
<button on:click={newNodeHandler}>
	NEW NODE
</button>