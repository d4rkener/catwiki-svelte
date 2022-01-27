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
      width: 150px;
      height: 150px;
      border-radius: 12px;

      @include md.breakpoint(medium) {
        width: 200px;
        height: 200px;
      }

      @include md.breakpoint(large) {
        width: 250px;
        height: 250px;
      }
    }

    &__name {
      color: var.$cannonBlack;
      font-weight: 600;
      font-size: 0.875rem;
      margin-top: 12px;

      @include md.breakpoint(medium) {
        font-size: 1.125rem;
      }
    }
  }
</style>
