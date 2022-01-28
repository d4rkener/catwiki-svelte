<div class="information">
  <div class="information__content">
    <h3 class="information__content--heading">Why should you have a cat?</h3>
    <p class="information__content--paragraph">
      Having a cat around you can actually trigger the release of calming chemicals in your body
      which lower your stress and anxiety leves
    </p>
    <a sveltekit:prefetch href="/why-cats"
      >Read More <img src="./arrow-forward-outline.svg" alt="arrow-logo" /></a
    >
  </div>
  <div class="information__images">
    <img src="./image-1.png" alt="cute-cat" />
    <img src="./image-2.png" alt="cute-cat" />
    <img src="./image-3.png" alt="cute-cat" />
  </div>
</div>

<style lang="scss">
  @use '../../scss/_variables.scss' as var;
  @use '../../scss/_breakpoints.scss' as md;

  .information {
    margin-top: 3.9375rem;

    @include md.breakpoint(large) {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 2rem;
    }

    &__content {
      flex: 1;

      &--heading {
        font-size: 2.5rem;
        font-weight: 700;
        color: var.$cannonBlack;
        position: relative;

        @include md.breakpoint(large) {
          font-size: 3rem;
        }

        &::before {
          content: '';
          position: absolute;
          top: -1rem;
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

      &--paragraph {
        font-size: 1.125rem;
        font-weight: 500;
        color: var.$cannonBlack;
        margin-top: 2.5rem;

        @include md.breakpoint(large) {
          width: 25rem;
        }
      }

      a {
        margin-top: 1.625rem;
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

    &__images {
      flex: 1;
      margin-top: 3.75rem;
      display: grid;
      grid-template-columns: repeat(6, 1fr);
      grid-template-rows: 2, 1fr;
      gap: 1rem;

      img:first-child {
        grid-column: 2 / 4;
        grid-row: 2 / 3;
      }

      img:nth-child(2) {
        grid-column: 1 / 4;
        grid-row: 1 / 2;
      }

      img:last-child {
        grid-column: 4 / 7;
        grid-row: 1 / 3;
      }
    }
  }
</style>
