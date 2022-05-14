<script>
  import Contribute from "./lib/Contribute.svelte";
  import List from "./lib/List.svelte";
</script>

<main>
  <List />
</main>
<Contribute />

<style lang="scss">
  :global(body) {
    background-color: var(--pale-gray);

    font-family: "Truculenta", sans-serif;
  }

  main {
    padding: 23px;
  }
</style>
