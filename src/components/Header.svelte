<script>
  // import Logo from './Logo.svelte';
  import Nav from './Nav.svelte';

  export let segment;
</script>

<style>
  header {
    width: 100vw;
    height: 56px;
    background-color: var(--var-header-bg);
    box-shadow: 0 0 2px #aaaaaa;
    margin: 0 auto;
    position: sticky;
    top: 0;
    z-index: 1000;
  }

  .header {
    display: flex;
    padding: 8px 22px;
    align-items: center;
    width: 100%;
    max-width: var(--max-width);
    /* max-width: var(--max-content-width); */
    margin: 0 auto;
  }

  .logo {
    font-size: 1.5em;
    font-weight: 600;
  }

  a {
    color: var(--var-text-primary);
    transition: color 0.5s cubic-bezier(0.28, 0.11, 0.32, 1);
    text-decoration: none;
  }
</style>

<header>
  <div class="header">
    <div class="logo"><a href="./">Sandip Nirmal</a></div>
    <Nav {segment} />
  </div>
</header>
