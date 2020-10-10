<script>
  // import Logo from './Logo.svelte';
  import Nav from './Nav.svelte';

  export let segment;
</script>

<style>
  header {
    margin: 0 auto;
    max-width: 1048px;
    width: 100%;
    height: 56px;
  }

  .header {
    display: flex;
    padding: 8px 24px;
    align-items: center;
  }

  h3 {
    background-color: #000000;
    color: #fff;
    border-radius: 50%;
    padding: 8px;
  }
</style>

<header>
  <div class="header">
    <h3>SN</h3>
    <Nav {segment} />
  </div>
</header>
