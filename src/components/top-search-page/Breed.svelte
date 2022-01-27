<script>
  export let result;
  export let index;

  index++;
</script>

<div class="breed">
  <a sveltekit:prefetch href="/cat/{result.id}">
    <img src={result.image.url} alt={result.name} class="breed__img" />
  </a>
  <div class="breed__information">
    <h3>{index}. {result.name}</h3>
    <p>{result.description}</p>
  </div>
</div>

<style lang="scss">
  @use '../../scss/_variables.scss' as var;
  @use '../../scss/_breakpoints.scss' as md;

  .breed {
    &:not(:last-child) {
      margin-bottom: 1.875rem;
    }

    @include md.breakpoint(large) {
      display: flex;
      align-items: flex-start;
      gap: 1.875rem;
    }

    &__img {
      width: 9.375rem;
      height: 9.375rem;
      border-radius: 0.75rem;

      @include md.breakpoint(medium) {
        width: 12.5rem;
        height: 12.5rem;
      }
    }

    &__information {
      margin-top: 1.25rem;

      h3 {
        color: var.$cannonBlack;
      }

      p {
        margin-top: 1.125rem;
        font-weight: 500;
        color: var.$cannonBlack;

        @include md.breakpoint(large) {
          max-width: 55.5rem;
        }
      }
    }
  }
</style>
