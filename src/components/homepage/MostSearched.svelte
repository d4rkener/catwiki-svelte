<div class="showcase">
  <p class="showcase__title">Most Searched Breeds</p>
  <div class="showcase__heading">
    <h1>66+ Breeds For you <br /> to discover</h1>
    <a href="/top-search">See More <img src="./arrow-forward-outline.svg" alt="arrow-logo" /></a>
  </div>
</div>

<style lang="scss">
  @use '../../scss/_variables.scss' as var;
  @use '../../scss/_breakpoints.scss' as md;

  .showcase {
    background-color: var.$westar;
    padding: 1.125rem 1.875rem;

    @include md.breakpoint(medium) {
      padding: 1.75rem 3.75rem;
    }

    @include md.breakpoint(large) {
      padding: 2.125rem 5.625rem;
    }

    &__title {
      font-size: 0.875rem;
      position: relative;
      color: var.$cannonBlack;

      @include md.breakpoint(medium) {
        font-size: 1rem;
      }

      @include md.breakpoint(large) {
        font-size: 1.125rem;
      }

      &::before {
        content: '';
        position: absolute;
        bottom: -0.3125rem;
        left: 0;
        width: 20%;
        height: 0.1875rem;
        background-color: var.$cioccolato;
        border-radius: 4.8125rem;

        @include md.breakpoint(medium) {
          width: 14%;
        }

        @include md.breakpoint(large) {
          width: 8%;
        }
      }
    }

    &__heading {
      margin-top: 1.25rem;
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      gap: 1.25rem;

      @include md.breakpoint(medium) {
        margin-top: 2.25rem;
      }

      h1 {
        font-size: 1.125rem;
        color: var.$cannonBlack;

        @include md.breakpoint(medium) {
          font-size: 1.75rem;
        }

        @include md.breakpoint(large) {
          font-size: 3rem;
        }
      }

      a {
        color: rgba(var.$cannonBlack, 0.6);
        font-weight: 700;
        display: flex;
        align-items: center;
        gap: 0.3125rem;
        font-size: 0.875rem;
        text-transform: uppercase;

        @include md.breakpoint(medium) {
          font-size: 1rem;
        }

        @include md.breakpoint(large) {
          font-size: 1.125rem;
        }

        img {
          width: 1.125rem;
        }
      }
    }
  }
</style>
