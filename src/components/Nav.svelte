<script>
  export let segment;

  let isDarkMode = false;

  if (process.browser) {
    const theme = localStorage.getItem('theme');

    if (theme) {
      isDarkMode = theme === 'dark';
    } else {
      isDarkMode = window.matchMedia('(prefers-color-scheme: dark)').matches;
    }

    const page = document.querySelector('html');
    page.setAttribute('data-theme', isDarkMode ? 'dark' : '');
  }

  const changeTheme = () => {
    if (process.browser) {
      const page = document.querySelector('html');
      isDarkMode = !isDarkMode;
      page.setAttribute('data-theme', isDarkMode ? 'dark' : '');
      localStorage.setItem('theme', isDarkMode ? 'dark' : 'light');
    }
  };
</script>

<style>
  nav {
    align-items: center;
    display: flex;
    flex: 1;
    justify-content: flex-end;
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

  button {
    background: transparent;
    text-align: center;
    font-size: 16px;
    cursor: pointer;
    outline: none;
  }

  @media (max-width: 480px) {
    a {
      margin-left: 8px;
    }
  }
</style>

<nav>
  <button
    title={isDarkMode ? 'Turn on the Light' : 'Dim the Light'}
    on:click={changeTheme}>{isDarkMode ? '☀️' : '🌒'}</button>
  <a class={segment === 'about' ? 'selected' : ''} href="about">About</a>
  <a
    rel="prefetch"
    class={segment === 'blog' ? 'selected' : ''}
    href="blog">Blog</a>
</nav>
