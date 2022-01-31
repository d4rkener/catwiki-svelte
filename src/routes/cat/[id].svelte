<script context="module">
  export const load = async ({ url, params }) => {
    const id = params.id;
    const res = await fetch(
      `https://api.thecatapi.com/v1/breeds/search?${import.meta.env.VITE_API_KEY}&q=${id}`
    );
    const data = await res.json();

    return { props: { id, data } };
  };
</script>

<script>
  import CatInformation from '../../components/cat-page/CatInformation.svelte';
  export let id, data;

  console.log(id, data);
</script>

<CatInformation />
