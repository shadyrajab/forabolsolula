<script>
  export let title;
  export let description;
  export let epoch_timestamp;
  export let id_page;

  $: formatedDate = new Date(epoch_timestamp * 1000).toLocaleDateString(
    "pt-BR",
    { dateStyle: "medium" }
  );

  let expanded = false;
</script>

<li class:expanded on:click={() => (expanded = !expanded)}>
  <a href={id_page}>
    <section>
      <header>
        <h1>
          {title}
        </h1>
      </header>
      <main>
        <p class="description">
          {description}
        </p>
      </main>
    </section>
  </a>
  <aside>
    <p>{formatedDate}</p>
  </aside>
</li>

<style lang="scss" scoped>
  li {
    position: relative;

    background-color: white;

    border: 1px solid transparent;
    border-radius: 5px;

    padding: 15px 10px 10px;
    margin-left: 20px;

    transition: 500ms;

    max-height: 300px;

    cursor: pointer;

    border: 1px solid transparent;

    &::before {
      content: "";

      width: 20px;
      height: 20px;

      border-radius: 50%;
      border: 2.5px solid #fff;

      background-color: #c33940;

      position: absolute;
      transform: translate(-50%, -50%);
      top: 22px;
      left: -22px;
    }
  }

  h1 {
    font-weight: 900;
    font-size: 1.2rem;

    margin-bottom: 10px;

    color: var(--blue-gray);
  }

  p {
    color: var(--gray);
  }

  aside {
    background-color: #c33940;

    text-align: center;

    padding: 5px 7.5px;

    border: 2.5px solid #fff;
    border-radius: 5px;

    position: absolute;
    top: -25px;
    right: 5px;

    p {
      font-size: 1rem;
      font-weight: 900;

      color: #ffffff;
    }
  }
</style>
