<script lang="ts">
  import svelteLogo from './assets/svelte.svg';
  import viteLogo from './assets/vite.svg';
  import tailwindLogo from './assets/tailwindcss.svg';

  import Counter from './lib/Counter.svelte';
</script>

<main>
  <div class="logo">
    <a href="https://svelte.dev" target="_blank" rel="noreferrer">
      <img src={svelteLogo} class="hover:drop-shadow-[0_0_2em_#ff3e00aa]" alt="Svelte Logo" />
    </a>
    <a href="https://vite.dev" target="_blank" rel="noreferrer">
      <img src={viteLogo} class="hover:drop-shadow-[0_0_2em_#646cffaa]" alt="Vite Logo" />
    </a>
    <a href="https://tailwindcss.com" target="_blank" rel="noreferrer">
      <img src={tailwindLogo} class="hover:drop-shadow-[0_0_2em_#00bcffaa]" alt="Tailwindcss Logo" />
    </a>
  </div>

  <h1>Svelte + Vite + Tailwindcss</h1>

  <div class="card">
    <Counter />
  </div>

  <p class="read-the-docs">Click on any logo to learn more</p>
</main>

<style lang="postcss">
  @reference "tailwindcss";

  main {
    @apply p-8 text-center;
  }
  .logo {
    @apply flex place-content-between;
  }
  .logo img {
    @apply m-6 size-24;
  }
  h1 {
    @apply my-8 text-4xl font-bold;
  }
  .card {
    @apply p-8;
  }
  .read-the-docs {
    @apply text-neutral-600 italic dark:text-neutral-400;
  }
</style>
