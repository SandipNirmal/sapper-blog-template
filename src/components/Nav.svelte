<script>
  export let segment;
</script>

<style>
  nav {
    align-items: flex-end;
    display: flex;
    flex: 1;
    font-weight: 700;
    justify-content: flex-end;
    text-transform: uppercase;
    font-size: 14px;
  }

  a {
    color: inherit;
    text-decoration: none;
    padding: 10px 5px;
    display: block;
    position: relative;
    margin-left: 20px;
  }

  a:not(.selected) {
    opacity: 0.7;
  }
</style>

<nav>
  <a class={segment === 'about' ? 'selected' : ''} href="about">about</a>
  <a
    rel="prefetch"
    class={segment === 'blog' ? 'selected' : ''}
    href="blog">blog</a>
</nav>
