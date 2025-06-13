<script lang="ts">
  import page from 'page';
  import Home from './pages/Home.svelte';
  import About from './pages/About.svelte';
  import Settings from './pages/Settings.svelte';

  let current = Home;

  page('/', () => (current = Home));
  page('/about', () => (current = About));
  page('/settings', () => (current = Settings));
  page.start();
</script>

<main>
  <nav>
    <a href="/">home</a>
    <a href="/about">about</a>
    <a href="/settings">Settings</a>
  </nav>

  <svelte:component this={current} />
</main>

<style lang="postcss">
  @reference "tailwindcss";

  main {
    @apply min-w-xs p-8 text-center;
  }
  nav {
    @apply mb-2 flex justify-between;
  }
</style>
