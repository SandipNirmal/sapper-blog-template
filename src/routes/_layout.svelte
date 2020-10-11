<script>
  import Header from '../components/Header.svelte';

  export let segment;
</script>

<style>
  .layout {
    display: flex;
    flex-direction: column;
    width: 100vw;
    margin: 0 auto;
    min-height: 100%;
    min-height: 100vh;
  }

  main {
    width: 100vw;
    margin: 0 auto;
    max-width: var(--max-width);
    flex: 1;
    position: relative;
    padding: 1em 2em;
    padding-top: 6em;
    box-sizing: border-box;
    width: 100%;
    display: flex;
    flex-direction: column;
  }

  @media (max-width: 480px) {
    main {
      padding-top: 4em;
    }
  }

  footer {
    width: 100vw;
    color: var(--var-secodary-color);
    font-size: 1em;
    text-align: center;
    /* background-color: var(--var-bg-footer); */
    margin-top: 2em;
  }

  .footer {
    max-width: var(--max-width);
    margin: 0 auto;
    padding: 4em 2em 1.5em;
  }
</style>

<div class="layout">
  <Header {segment} />

  <main>
    <slot />
  </main>

  <footer>
    <div class="footer">
      <span>
        <!-- By: Sandip Nirmal. -->
        
        
        Made with
        <a
          href="https://sapper.svelte.dev"
          rel="noreferrer"
          target="_blank">Sapper</a>.
      </span>
    </div>
  </footer>
</div>
