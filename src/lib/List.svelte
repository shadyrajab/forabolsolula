<script>
  import Card from "./Card.svelte";

  async function request() {
    const response = await fetch("http://localhost:3000/forabolsonaro");
    const json = await response.json();

    return json;
  }

  const promise = request();
</script>

<ul>
  {#await promise}
    <p>loading</p>
  {:then news}
    {#each news.sort((a, b) => a - b) as item}
      <Card {...item} />
    {/each}
  {:catch error}
    <p>fail</p>
  {/await}
</ul>

<style lang="scss">
  ul {
    display: flex;
    flex-flow: column nowrap;
    row-gap: 40px;

    padding: 50px 0;

    min-height: 100vh;

    border-left: 5px solid #c0c8d1;

    position: relative;
  }
</style>
