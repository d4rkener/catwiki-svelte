<nav class="navbar">
  <a href="/">
    <img src="./catwiki-logo-dark.svg" alt="logo" />
  </a>
</nav>

<style lang="scss">
  @use '../scss/_breakpoints.scss' as md;

  .navbar {
    margin: 0.75rem 0;

    @include md.breakpoint(medium) {
      margin: 1.125rem 0;
    }
  }
</style>
