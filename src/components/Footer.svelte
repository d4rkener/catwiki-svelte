<footer class="footer">
  <img src="./catwiki-logo-light.svg" alt="logo" class="footer__logo" />
  <p class="footer__paragraph">
    &#169; created by <a href="https://github.com/rahulshawdev/" target="_blank">rahulshawdev</a>
  </p>
</footer>

<style lang="scss">
  @use '../scss/_variables.scss' as var;
  @use '../scss/_breakpoints.scss' as md;

  .footer {
    background-color: var.$black;
    margin-top: 1.5rem;
    border-top-left-radius: 2.625rem;
    border-top-right-radius: 2.625rem;
    padding: 1.875rem;
    color: var.$white;

    @include md.breakpoint(medium) {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    @include md.breakpoint(large) {
      margin-top: 6.25rem;
    }

    &__logo {
      width: 7.9375rem;
    }

    &__paragraph {
      font-size: 0.9375rem;

      @include md.breakpoint(medium) {
        font-size: 1.125rem;
      }

      a {
        color: var.$white;
        font-weight: 700;
        text-decoration: underline;
      }
    }
  }
</style>
