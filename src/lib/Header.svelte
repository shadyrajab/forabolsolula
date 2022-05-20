<script>
  let scrollY;

  let minimized = false;

  $: {
    if (80 - scrollY < 40) {
      minimized = true;
    } else {
      minimized = false;
    }
  }
</script>

<svelte:window bind:scrollY />

<header style={`height: ${80 - scrollY}px`} />

<style lang="scss">
  header {
    position: fixed;
    z-index: 1;

    background: #737980;

    color: #e9f1f4;

    width: 100%;
    min-height: 50px;
    padding: 10px;

    box-shadow: 0 0 5px darken(#f6f9faa8, 80%);
  }
</style>
