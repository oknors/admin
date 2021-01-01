<script>
  import { onMount } from 'svelte';

  export let apiURL

  export let posts = [];

  onMount(async () => {
    const res = await fetch(apiURL);
    posts = await res.json();
  });

</script>
