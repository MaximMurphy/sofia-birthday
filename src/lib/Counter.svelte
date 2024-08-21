<script lang="ts">
  import Sparkles from '../lib/Sparkles.svelte';
  let count: number = 0
  const increment = () => {
    if (count < 21){
      count += 1
    }
  }
</script>

<!-- Conditional render for counter view -->
{#if count < 21}
	<h2>How old are you today?</h2>
  <button on:click={increment}>
  {count} years old
</button>
{/if}

<!-- Conditional render for birthday view -->
{#if count === 21}
  <h1>HAPPY BIRTHDAY <span class="sofia">SOFIA</span>! </h1> 
  <Sparkles />
{/if}

<style>
  button {
    width: 150px;
    height: 75px;
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
