<script>
  export let result;
</script>

<div class="cat">
  <a href="/cat/{result.id}">
    <img src={result.image.url} alt={result.name} class="cat__image" />
    <h3 class="cat__name">{result.name}</h3>
  </a>
</div>

<style lang="scss">
  @use '../../scss/_variables.scss' as var;
  @use '../../scss/_breakpoints.scss' as md;

  .cat {
    &__image {
      width: 9.375rem;
      height: 9.375rem;
      border-radius: 0.75rem;

      @include md.breakpoint(medium) {
        width: 12.5rem;
        height: 12.5rem;
      }

      @include md.breakpoint(large) {
        width: 15.625rem;
        height: 15.625rem;
      }
    }

    &__name {
      color: var.$cannonBlack;
      font-weight: 600;
      font-size: 0.875rem;
      margin-top: 0.75rem;

      @include md.breakpoint(medium) {
        font-size: 1.125rem;
      }
    }
  }
</style>
