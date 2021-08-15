<script>
  import Account from './components/Account.svelte';

  for (let index = 0; index < 10; index++) {}
</script>

<main>
  {#each Array.from(Array(50).keys()) as index}
    <Account />
  {/each}
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
