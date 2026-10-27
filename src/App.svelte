<script>
  import Cell from './Cell.svelte';

  let cells = $state([false, false, false, false]);

  let count = $derived(cells.filter((isOn) => isOn).length);

  function toggleCell(index) {
    cells[index] = !cells[index];
  }
</script>

<main class="container">
  <h1 class="count-display">Count: {count}</h1>

  <div class="grid">
    {#each cells as isOn, index}
      <Cell {isOn} {index} toggle={() => toggleCell(index)} />
    {/each}
  </div>
</main>

<style>
  .container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
    font-family: sans-serif;
  }

  .count-display {
    font-size: 2rem;
    font-weight: bold;
    margin-bottom: 20px;
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(2, 100px);
    grid-template-rows: repeat(2, 100px);
    gap: 0;
  }
</style>
