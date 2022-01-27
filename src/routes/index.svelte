<script context="module">
  export const load = async () => {
    const res = await fetch(
      `https://api.thecatapi.com/v1/breeds?${import.meta.env.VITE_API_KEY}&limit=4`
    );

    const data = await res.json();

    return { props: { results: data } };
  };
</script>

<script>
  import Hero from '../components/homepage/Hero.svelte';
  import MostSearched from '../components/homepage/MostSearched.svelte';
  import WhyCat from '../components/homepage/WhyCat.svelte';

  export let results;
</script>

<svelte:head>
  <title>CatWiki | Homepage</title>
</svelte:head>

<div class="index">
  <Hero />
  <MostSearched {results} />
  <WhyCat />
</div>
