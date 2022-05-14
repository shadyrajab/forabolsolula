<script>
  import Contribute from "./lib/Contribute.svelte";
  import List from "./lib/List.svelte";
</script>

<main>
  <List />
  <Contribute />
</main>

<style lang="scss">
  :global(body) {
    background-color: var(--pale-gray);

    font-family: "Truculenta", sans-serif;
  }

  main {
    width: 90vw;
    margin: 0 auto;
  }
</style>
