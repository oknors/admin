<script>
  // core components
  import DatePicker from "components/Utils/DatePicker.svelte";
  // export let location;
</script>

<div
  class="relative flex flex-col min-w-0 break-words w-full mb-6 shadow-lg rounded-lg bg-gray-200 border-0"
>
  <div class="rounded-t bg-white mb-0 px-6 py-6">
    <div class="text-center flex justify-between">
      <h6 class="text-gray-800 text-xl font-bold">Edit</h6>
      <button
        class="bg-red-500 text-white active:bg-red-600 font-bold uppercase text-xs px-4 py-2 rounded shadow hover:shadow-md outline-none focus:outline-none mr-1 ease-linear transition-all duration-150"
        type="button"
      >
        Save
      </button>
    </div>
  </div>
  <div class="flex-auto px-4 lg:px-10 py-10 pt-0">
    <form>
      <h6 class="text-gray-500 text-sm mt-3 mb-6 font-bold uppercase">
        Header
      </h6>
      <div class="flex flex-wrap">
        <div class="w-full lg:w-12/12 px-4">
          <div class="relative w-full mb-3">
            <label
              class="block uppercase text-gray-700 text-xs font-bold mb-2"
              for="grid-username"
            >
              ID
            </label>
            <input
              id="grid-username"
              type="text"
              class="px-3 py-3 placeholder-gray-400 text-gray-700 bg-white rounded text-sm shadow focus:outline-none focus:shadow-outline w-full ease-linear transition-all duration-150"
              value="lucky.jesse"
            />
          </div>
        </div>
        <div class="w-full lg:w-12/12 px-4">
          <div class="relative w-full mb-3">
            <label
              class="block uppercase text-gray-700 text-xs font-bold mb-2"
              for="grid-email"
            >
              Title
            </label>
            <input
              id="grid-email"
              type="email"
              class="px-3 py-3 placeholder-gray-400 text-gray-700 bg-white rounded text-sm shadow focus:outline-none focus:shadow-outline w-full ease-linear transition-all duration-150"
              value="jesse@example.com"
            />
          </div>
        </div>
        <div class="w-full lg:w-12/12 px-4">
          <div class="relative w-full mb-3">
            <label
              class="block uppercase text-gray-700 text-xs font-bold mb-2"
              for="grid-first-name"
            >
              Slug
            </label>
            <input
              id="grid-first-name"
              type="text"
              class="px-3 py-3 placeholder-gray-400 text-gray-700 bg-white rounded text-sm shadow focus:outline-none focus:shadow-outline w-full ease-linear transition-all duration-150"
              value="Lucky"
            />
          </div>
        </div>
      </div>

      <hr class="mt-6 border-b-1 border-gray-400" />

      <h6 class="text-gray-500 text-sm mt-3 mb-6 font-bold uppercase">
        Meta
      </h6>
      <div class="flex flex-wrap">
        <div class="w-full lg:w-6/12 px-6">
          <DatePicker dateLabel="Date created" dateElement="created" />
        </div>
        <div class="w-full lg:w-6/12 px-6">
          <DatePicker dateLabel="Date modified" dateElement="modified" />
        </div>
        <div class="w-full lg:w-4/12 px-4">
          <div class="relative w-full mb-3">
            <label
              class="block uppercase text-gray-700 text-xs font-bold mb-2"
              for="grid-type"
            >
              Type
            </label>
            <select id="grid-type"
                    class="px-3 py-3 placeholder-gray-400 text-gray-700 bg-white rounded text-sm shadow focus:outline-none focus:shadow-outline w-full ease-linear transition-all duration-150">
              <option>Post</option>
              <option>Page</option>
              <option>Media</option>
              <option>Other</option>
            </select>
          </div>
        </div>
        <div class="w-full lg:w-4/12 px-4">
          <div class="relative w-full mb-3">
            <label
              class="block uppercase text-gray-700 text-xs font-bold mb-2"
              for="grid-template"
            >
              Template
            </label>
            <select id="grid-template"
                    class="px-3 py-3 placeholder-gray-400 text-gray-700 bg-white rounded text-sm shadow focus:outline-none focus:shadow-outline w-full ease-linear transition-all duration-150">
              <option>Post</option>
              <option>Page</option>
              <option>Media</option>
              <option>Other</option>
            </select>
          </div>
        </div>
        <div class="w-full lg:w-4/12 px-4">
          <div class="relative w-full mb-3">
            <label
              class="block uppercase text-gray-700 text-xs font-bold mb-2"
              for="grid-status"
            >
              Status
            </label>
            <select id="grid-status"
                    class="px-3 py-3 placeholder-gray-400 text-gray-700 bg-white rounded text-sm shadow focus:outline-none focus:shadow-outline w-full ease-linear transition-all duration-150">
              <option>Draft</option>
              <option>Published</option>
              <option>Not Published</option>
              <option>Other</option>
            </select>
          </div>
        </div>
      </div>

      <hr class="mt-6 border-b-1 border-gray-400" />

      <h6 class="text-gray-500 text-sm mt-3 mb-6 font-bold uppercase">
        Content
      </h6>
      <div class="flex flex-wrap">
        <div class="w-full lg:w-12/12 px-4">
          <div class="relative w-full mb-3">
            <label
              class="block uppercase text-gray-700 text-xs font-bold mb-2"
              for="grid-about-me"
            >
              Main content
            </label>
            <textarea
              id="grid-about-me"
              type="text"
              class="px-3 py-3 placeholder-gray-400 text-gray-700 bg-white rounded text-sm shadow focus:outline-none focus:shadow-outline w-full ease-linear transition-all duration-150"
              rows="4"
              value="A beautiful UI Kit and Admin for Svelte & Tailwind CSS. It is Free
                and Open Source."
            />
          </div>
        </div>
      </div>
    </form>
  </div>
</div>
