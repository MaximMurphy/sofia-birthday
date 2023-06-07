<script lang="ts">
  import Sparkles from '../lib/Sparkles.svelte';
  let count: number = 0
  const increment = () => {
    if (count < 20){
      count += 1
    }
  }
</script>

{#if count < 20}
	<h2>How old are you today?</h2>
  <button on:click={increment}>
  {count} years old
</button>
{/if}
{#if count === 20}
  <h1>HAPPY BIRTHDAY <span class="sofia">SOFIA</span>! </h1> 
  <Sparkles />
{/if}

<style>
  button {
    width: 10vw;
    height: 5vw;
    padding: 10px;
    background-image: linear-gradient(to bottom right, orange, yellow);
    border: solid 2px white;
    border-radius: 8px;
    font-size: large;
    cursor: pointer;
    color: black;
    font-weight: bold;
  }
  button:hover {
    background-image: linear-gradient(to bottom right, yellow, orange);
  }
</style>
