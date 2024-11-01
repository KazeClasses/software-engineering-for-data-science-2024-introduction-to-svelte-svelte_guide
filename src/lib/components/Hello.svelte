<script>
  let name = 'world';
  let pokeCount = 0;

  function handlePoke() {
    pokeCount += 1;
  }
</script>

<input bind:value={name} placeholder="Enter your name" />
<p>Hello {name}!</p>

<button on:click={handlePoke}>
  Poked {pokeCount} {pokeCount === 1 ? 'time' : 'times'}
</button>

{#if pokeCount > 10}
  <p>You are annoying</p>
{/if}

