<script>
	import Nested from "./Nested.svelte";
  export let depth = 0;
</script>


<div class="recursive-component">
  <p>Depth: {depth}</p>
  
  {#if depth < 5}
    <Nested depth={depth + 1}>
      <p>Custom content for depth {depth + 1}</p>
    </Nested>
  {/if}
</div>

<style>
  .recursive-component {
    margin-left: 10px;
    padding: 10px;
    border: 1px solid #ccc;
  }
</style>
