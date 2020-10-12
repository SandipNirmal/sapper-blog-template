<script context="module">
  export async function preload({ params, query }) {
    // the `slug` parameter is available because
    // this file is called [slug].html
    const res = await this.fetch(`blog/${params.slug}.json`);
    const data = await res.json();

    if (res.status === 200) {
      return { post: data };
    } else {
      this.error(res.status, data.message);
    }
  }
</script>

<script>
  export let post;
</script>

<style>
  header {
    text-align: center;
    padding-bottom: 16px;
  }

  header h1 {
    margin-bottom: 0.5em;
  }

  header span {
    color: var(--var-text-secondary);
    text-transform: uppercase;
    font-size: 0.75em;
  }
</style>

<svelte:head>
  <title>{post.title}</title>
</svelte:head>

<header>
  <h1>{post.title}</h1>
  <span>{post.printDate.toLowerCase() === 'invalid date' ? post.date : post.printDate}
    -
    {post.printReadingTime}</span>
</header>
<div class="container">
  <article class="content">
    {@html post.html}
  </article>
  <!-- <hr /> -->
</div>
