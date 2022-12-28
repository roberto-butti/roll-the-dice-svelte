<script>
  import svelteLogo from './assets/svelte.svg'
  import RollTheDice from './lib/RollTheDice.svelte'
</script>

<main>
  <div>
    <a href="https://vitejs.dev" target="_blank" rel="noreferrer">
      <img src="/vite.svg" class="logo" alt="Vite Logo" />
    </a>
    <a href="https://svelte.dev" target="_blank" rel="noreferrer">
      <img src={svelteLogo} class="logo svelte" alt="Svelte Logo" />
    </a>
  </div>
  <h1>Roll the dice with Vite and Svelte</h1>

  <div class="card">
    <RollTheDice />
  </div>

  <p>
    Check out <a href="https://github.com/roberto-butti/roll-the-dice-svelte" target="_blank" rel="noreferrer">Source code</a>.
  </p>

  <p class="read-the-docs">
    Click on the Vite and Svelte logos to learn more
  </p>
</main>

<style>
  .logo {
    height: 4em;
    padding: 1em;
    will-change: filter;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
  .read-the-docs {
    color: #888;
  }
</style>
