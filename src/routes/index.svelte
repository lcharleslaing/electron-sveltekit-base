<script>
</script>

<svelte:head>
  <title>Electron / Sveltekit Base</title>
</svelte:head>

<main>
  <h2 class="text-primary">Electron/Sveltekit Base!</h2>
  <p>Clone this and make it your own!</p>
  <p>
    <a
      target="_blank"
      href="https://github.com/lcharleslaing/electron-sveltekit-base.git"
      class="button">My Repository</a
    >
  </p>
</main>

<style lang="scss">
  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }

  h1 {
    text-transform: uppercase;
    font-size: 4rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 4rem auto;
    max-width: 14rem;
  }

  p {
    max-width: 14rem;
    margin: 2rem auto;
    line-height: 1.35;
  }

  @media (min-width: 480px) {
    h1 {
      max-width: none;
    }

    p {
      max-width: none;
    }
  }
</style>
