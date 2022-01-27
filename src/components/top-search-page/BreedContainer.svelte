<script>
  import Breed from './Breed.svelte';

  export let results;
</script>

<div class="breeds-container">
  {#each results as result, index (result.id)}
    <Breed {result} {index} />
  {/each}
</div>

<style lang="scss">
  @use '../../scss/_breakpoints.scss' as md;

  .breeds-container {
    margin-top: 1.5rem;

    @include md.breakpoint(large) {
      margin-top: 3.25rem;
    }
  }
</style>
