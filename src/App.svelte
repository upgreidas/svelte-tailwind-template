<script lang="ts">
  import Tailwind from './Tailwind.svelte';

  export let name: string;
</script>

<Tailwind />

<main>
  <h1>Hello {name}!</h1>
  <button class="app-btn">HELLO</button>
</main>

<style lang="scss">
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }

  .app-btn {
    @apply text-black;
    @apply rounded-full;
    @apply py-1;
    @apply px-4;
    @apply shadow;

    &:hover {
      @apply bg-blue-700;
      @apply text-white;
    }
  }
</style>
