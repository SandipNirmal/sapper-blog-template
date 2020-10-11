<script>
  // import Logo from './Logo.svelte';
  import Nav from './Nav.svelte';

  export let segment;
</script>

<style>
  header {
    width: 100vw;
    height: 56px;
    margin: 0 auto;
    max-width: var(--max-width);
  }

  .header {
    display: flex;
    padding: 8px;
    align-items: center;
    width: 100%;
    max-width: var(--max-content-width);
    margin: 0 auto;
  }
</style>

<header>
  <div class="header">
    <h3>SN</h3>
    <Nav {segment} />
  </div>
</header>
