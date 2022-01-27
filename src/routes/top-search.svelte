<script context="module">
  export const load = async () => {
    const res = await fetch(
      `https://api.thecatapi.com/v1/breeds?${import.meta.env.VITE_API_KEY}&limit=10`
    );

    const data = await res.json();

    return { props: { results: data } };
  };
</script>

<script>
  import BreedContainer from '../components/top-search-page/BreedContainer.svelte';

  export let results;
</script>

<svelte:head>
  <title>CatWiki | Top Searched Breeds</title>
</svelte:head>

<div class="top-search">
  <h2 class="top-search__heading">Top 10 most searched breeds</h2>
  <BreedContainer {results} />
</div>

<style lang="scss">
  @use '../scss/_variables.scss' as var;
  @use '../scss/_breakpoints.scss' as md;

  .top-search {
    &__heading {
      font-size: 1.5rem;
      color: var.$cannonBlack;
      font-weight: 700;

      @include md.breakpoint(medium) {
        font-size: 2.25rem;
      }
    }
  }
</style>
