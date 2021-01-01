<script>
// core components

import { onMount } from 'svelte';

import { link } from "svelte-routing";

export let apiURL

export let hosts = [];

onMount(async () => {
  const res = await fetch(apiURL+"cms/hosts");
  hosts = await res.json();
});
  // can be one of light or dark
  export let color = "light";


  import { slide } from 'svelte/transition';
  let visible = true;


  const expand = (host) => {
    hosts = hosts.map(s => {
    s.active = false
    if (s.slug === host.slug) {
      s.active = true
    }
    return s
  })
}
</script>


{#each hosts as host}
  <!-- Heading -->
  <button on:click={() => expand(host) }
    class="md:min-w-full text-gray-600 text-xs text-left uppercase font-bold block pt-2 pb-2 no-underline"
  >
    {host.host}
  </button>
  <!-- Navigation -->
    {#if host.active}
      <div class="slider" transition:slide>
        <ul class="md:flex-col md:min-w-full flex flex-col list-none md:mb-4">
          <li class="items-center">
            <a
              use:link
              class="text-gray-800 hover:text-gray-600 text-xs uppercase py-3 font-bold block"
              href="/admin/{ host.slug }/list"
            >
              <i class="fas fa-newspaper text-gray-400 mr-2 text-sm"></i>
              List
            </a>
          </li>
          <li class="items-center">
            <a
              use:link
              class="text-gray-800 hover:text-gray-600 text-xs uppercase py-3 font-bold block"
              href="/admin/create"
            >
              <i class="fas fa-newspaper text-gray-400 mr-2 text-sm"></i>
              Create
            </a>
          </li>
          <li class="items-center">
            <a
              use:link
              class="text-gray-800 hover:text-gray-600 text-xs uppercase py-3 font-bold block"
              href="/admin/edit"
            >
              <i class="fas fa-newspaper text-gray-400 mr-2 text-sm"></i>
              Edit
            </a>
          </li>

          <li class="items-center">
            <a
              use:link
              class="text-gray-800 hover:text-gray-600 text-xs uppercase py-3 font-bold block"
              href="/admin/edit"
            >
              <i class="fas fa-user-circle text-gray-400 mr-2 text-sm"></i>
              Settings
            </a>
          </li>
        </ul>
      </div>
    {/if}

  <!-- Divider -->
  <hr class="md:min-w-full" />

{/each}


