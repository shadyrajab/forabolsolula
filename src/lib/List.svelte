<script>
  import Card from "./Card.svelte";

  async function request() {
    const response = await fetch(
      "https://shadyrajab.github.io/forabolsolula/forabolsonaro.json"
    );
    const json = await response.json();

    return json;
  }

  const promise = request();
</script>

<ul>
  {#await promise}
    <p>loading</p>
  {:then news}
    {#each news.sort((a, b) => a - b) as item, index}
      <Card {...item} {index} />
    {/each}
  {:catch error}
    <p>fail</p>
  {/await}
</ul>

<style lang="scss">
  ul {
    display: grid;

    grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));

    gap: 20px;
  }
</style>
