<script context="module">
  export function preload({ params, query }) {
    return this.fetch(`blog.json`)
      .then((r) => r.json())
      .then((posts) => {
        return { posts };
      });
  }
</script>

<script>
  export let posts;

  console.log('Posts', posts)
</script>

<style>
  h2 {
    margin-top: 1em;
  }

  p {
    margin: 8px 0;
  }

  h2,
  .post-item-footer {
    font-weight: 700;
  }

  .post-item-date {
    color: var(--var-secodary-color);
    text-align: left;
    margin-right: 16px;
    font-size: 0.875em;
  }

  hr {
    margin: 32px auto;
  }
</style>

<svelte:head>
  <title>Sapper Blog Template | Blog</title>
</svelte:head>

<div class="container">
  <h1>Blog</h1>
  {#each posts as post, index}
    {#if index}
      <hr />
    {/if}
    <div class="post-item">
      <h2><a rel="prefetch" href="blog/{post.slug}">{post.title}</a></h2>
      <p>{post.excerpt}</p>
      <div class="post-item-footer">
        <span class="post-item-date">— {post.printDate.toLowerCase() === 'invalid date' ? post.date : post.printDate}</span>
      </div>
    </div>
  {/each}
</div>
