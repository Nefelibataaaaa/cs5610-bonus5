<script>
  let { isOn, index, toggle } = $props();
</script>

<button
  class="cell"
  class:on={isOn}
  onclick={toggle}
  type="button"
  aria-label="Cell {index + 1}"
  aria-pressed={isOn}
></button>

<style>
  .cell {
    width: 100px;
    height: 100px;
    background-color: white;
    border: 1px solid grey;
    cursor: pointer;
    box-sizing: border-box;
    padding: 0;
  }

  .cell:focus-visible {
    outline: 2px solid #4a90d9;
    outline-offset: 2px;
  }

  .cell.on {
    background-color: black;
  }
</style>
