<script>
  import { Link } from "svelte-navigator";
  let place = 1;
  //Función para cambiar las clases del botón
  function changePlace(change) {
    place = change;
  }
</script>

<header class="shadow-sm sticky top-0" style="background-color: #2E3440;">
  <div class="max-w-screen-xl p-4 mx-auto">
    <div class="flex items-center justify-between space-x-4 lg:space-x-10">
      <nav class="space-x-8 text-sm font-normal md:flex">
        <Link style="color:#ECEFF4;" to="/">
          <button
            on:click={()=>changePlace(1)}
            class={place === 1
              ? "inline-block px-12 py-3 text-white rounded-full group font-bold bg-slate-600"
              : "inline-block px-12 py-3 text-white rounded-full group font-bold"}
          >
            Inicio
          </button>
        </Link>
        <Link style="color:#ECEFF4;" to="tutoriales">
          <button
            on:click={()=>changePlace(2)}
            class={place === 2
              ? "inline-block px-12 py-3 text-white rounded-full group font-bold bg-slate-600"
              : "inline-block px-12 py-3 text-white rounded-full group font-bold"}
          >
            Tutoriales
          </button>
        </Link>
      </nav>
    </div>
  </div>
</header>
