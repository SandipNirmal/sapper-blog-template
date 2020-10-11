<script>
  export let segment;
</script>

<style>
  nav {
    align-items: flex-end;
    display: flex;
    flex: 1;
    justify-content: flex-end;
    /* font-size: 14px; */
  }

  a {
    color: inherit;
    text-decoration: none;
    padding: 10px 5px;
    display: block;
    position: relative;
    margin-left: 20px;
  }

  a.selected,
  a:focus,
  a:hover {
    color: var(--var-link-color);
  }

  a:not(.selected) {
    opacity: 0.88;
  }
</style>

<nav>
  <a class={segment === 'about' ? 'selected' : ''} href="about">About</a>
  <a
    rel="prefetch"
    class={segment === 'blog' ? 'selected' : ''}
    href="blog">Blog</a>
</nav>
