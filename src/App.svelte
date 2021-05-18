<script lang="ts">
  export let name: string;

  import { Array2D } from "/Users/bbtgnn/Documents/GitHub/array2D/dist";

  const grid = new Array2D<number>(5, 3);
  console.log(grid);
</script>

<main>
  {#each grid.content as row}
    <div class="row">
      {#each row as item}
        <div class="cell">{item.content}</div>
      {/each}
    </div>
  {/each}
</main>

<style>
  main {
    display: block;
  }
  .row {
    display: block;
  }
  .cell {
    display: inline-block;
    border: 2px solid black;
    padding: 4px;
  }
</style>
