<script>
  // core components
  import ListPosts from "components/Posts/ListPosts.svelte";

  export let apiURL
  export let location;
</script>

<div class="flex flex-wrap mt-4">
  <div class="w-full mb-12 px-4">
    <ListPosts color="dark" apiURL={apiURL} />
  </div>
</div>
