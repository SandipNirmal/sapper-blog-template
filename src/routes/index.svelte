<style>
  .home-container {
    align-items: center;
    display: flex;
    flex: 1;
    justify-content: center;
    /* margin: 2em 0; */
    min-height: 400px;
  }

  .home-copy {
    flex: 1;
  }

  h1 {
    font-weight: 700;
    margin-bottom: 0.5em;
  }

  @media (max-width: 800px) {
    .home-container {
      flex-direction: column;
    }

    .home-copy {
      flex: 0;
      padding-bottom: 2em;
      text-align: center;
    }
  }
</style>

<svelte:head>
  <title>Sapper Blog Template</title>
</svelte:head>

<div class="home-container">
  <div class="home-copy">
    <h1>Welcome to your new Sapper Blog.</h1>
    <p>
      This is a blog cum personal website template created using
      <a href="https://sapper.svelte.com" rel="noopener">Sapper</a>. You can
      write your blog as a markdown and you are done.
    </p>

    <p>
      Try adding new markdown file under
      <code>src/routes/blog/posts/</code>. This will serve as new blog post.
    </p>
  </div>
</div>
