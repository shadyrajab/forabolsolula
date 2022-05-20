<script>
  import Contribute from "./lib/Contribute.svelte";
  import Header from "./lib/Header.svelte";
  import List from "./lib/List.svelte";
</script>

<Header />
<main>
  <List />
  <Contribute />
</main>
<footer style="height: 50px" />

<style lang="scss">
  :global(body) {
    background-color: #e9f1f4;
    font-family: "Truculenta", sans-serif;
  }

  main {
    width: 95vw;
    margin: 0 auto;
    padding-top: 100px;
  }
</style>
