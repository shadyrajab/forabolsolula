<script>
  import Card from "./Card.svelte";
</script>

<ul>
  <Card />
  <Card />
  <Card />
</ul>

<style lang="scss">
  ul {
    display: flex;
    flex-flow: column nowrap;
    row-gap: 20px;

    padding: 20px;

    border-left: 5px solid #c0c8d1;

    position: relative;

    &::before,
    &::after {
      content: "";

      position: absolute;

      transform: translateX(-50%);

      width: 30px;
      height: 5px;
    }

    &::before {
      border-top: 5px solid #c0c8d1;
      top: 0;
      left: 0;
    }

    &::after {
      border-bottom: 5px solid #c0c8d1;
      bottom: 0;
      left: 0;
    }
  }
</style>
