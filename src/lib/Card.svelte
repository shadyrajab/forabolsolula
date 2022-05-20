<script>
  export let title;
  export let description;
  export let epoch_timestamp;
  export let id_page;
  export let index;
  export let hashtags = [];
  export let source = [];

  $: formatedDate = new Date(epoch_timestamp * 1000).toLocaleDateString(
    "pt-BR",
    { dateStyle: "medium" }
  );
</script>

<li class="container" style={`animation-duration: ${++index * 300}ms`}>
  <a href={source[0]} target="_blank" rel="noreferrer noopener">
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
    <footer>
      <ul>
        {#each hashtags as item}
          <li>{item}</li>
        {/each}
      </ul>
    </footer>
    <aside>
      <p>
        {formatedDate}
      </p>
    </aside>
  </a>
</li>

<style lang="scss">
  .container {
    position: relative;
    animation-name: appear;
    animation-fill-mode: forwards;

    a {
      display: block;
      background-color: #ffffff;
      border-radius: 5px;

      width: 100%;
    }

    main {
      padding: 10px;
    }

    h1 {
      font-size: 1.2rem;
      border-radius: 5px 5px 0 0;

      letter-spacing: 0.5px;
      font-weight: 900;

      margin-right: 10px;
      padding: 10px 5px 5px 10px;

      color: #313f49;
    }
  }

  footer {
    padding-left: 10px;
    padding-bottom: 30px;

    ul {
      display: flex;
      flex-flow: row wrap;

      gap: 7.5px;

      font-weight: bold;

      color: #c33940;

      li::before {
        content: "#";
      }
    }
  }

  aside {
    position: absolute;

    right: 10px;
    bottom: 10px;

    p {
      font-size: 0.9rem;
      font-weight: 900;

      text-transform: uppercase;
      text-align: right;

      letter-spacing: 1px;
    }
  }

  p {
    color: #737980;
  }
</style>
