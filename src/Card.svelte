<script>
  export let name, content, type, duration, link;
</script>

<article
  class="p-6 sm:p-8 rounded-xl drop-shadow-md"
  style="background-color: #D8DEE9;"
>
  <div class="flex items-start">
    <div
      class="hidden sm:grid sm:h-20 sm:w-20 sm:shrink-0 sm:place-content-center sm:rounded-full sm:border-2 sm:border-gray-700"
      aria-hidden="true"
    >
      <div class="flex items-center gap-1">
        <span class="material-icons text-gray-700" style="font-size: 3rem;">
          dvr
        </span>
      </div>
    </div>

    <div class="sm:ml-8">
      <strong
        class="rounded border px-3 py-1.5 text-[10px] font-medium text-white"
        style="background-color: #D08770;"
      >
        {type}
      </strong>

      <h2 class="mt-4 text-lg font-medium sm:text-xl" style="color: #2E3440;">
        <a href={link} target="__blank" class="hover:underline"> {name} </a>
      </h2>

      <p class="mt-1 text-sm" style="color: #3B4252;">
        {content}
      </p>

      <div class="mt-4 sm:flex sm:items-center sm:gap-2">
        <div class="flex items-center text-gray-500">
          <svg
            class="w-4 h-4"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"
            />
          </svg>
          <p class="ml-1 text-xs font-medium">{duration}</p>
        </div>

        <span class="hidden sm:block" aria-hidden="true">&middot;</span>

        <p class="mt-2 text-xs font-medium text-gray-500 sm:mt-0">
          Hecho por ElmudoFreeman
        </p>
      </div>
    </div>
  </div>
</article>
