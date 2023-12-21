<script>
  import { fade } from 'svelte/transition';

  let visible = false;

  function toggleVisibility() {
    visible = !visible;
  }
</script>

<style>
  .box {
    width: 100px;
    height: 100px;
    background-color: #3498db;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #fff;
    font-size: 1.2rem;
  }
</style>

<button on:click={toggleVisibility}>Toggle Visibility</button>

{#if visible}
  <div transition:fade class="box">
    Hello, Svelte!
  </div>
{/if}
