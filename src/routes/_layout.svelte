<script>
  import Header from '../components/Header.svelte';

  export let segment;
</script>

<style>
  .layout {
    display: flex;
    flex-direction: column;
    width: 100%;
    max-width: 1440px;
    margin: 0 auto;
    min-height: 100%;
    min-height: 100vh;
  }

  main {
    flex: 1;
    position: relative;
    margin: 0 auto;
    max-width: 1280px;
    background-color: white;
    padding: 1em 2em;
    box-sizing: border-box;
    width: 100%;
    display: flex;
    flex-direction: column;
  }

  footer {
    color: #aaa;
    font-size: 1em;
    margin: 1em auto;
    padding: 1em 2em;
    text-align: center;
    width: 100%;
  }
</style>

<div class="layout">
  <Header {segment} />

  <main>
    <slot />
  </main>

  <footer>
    <span>
      By: Sandip Nirmal.
      Made with <a href="https://sapper.svelte.dev" target="_blank">Sapper</a>.
    </span>
  </footer>
</div>
