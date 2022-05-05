<script>
  import Card from "./Card.svelte";

  let promise = getAllArticles();

  async function getAllArticles() {
    const res = await fetch(
      "#######",
      {
        headers: {
          apikey:
            "#########",
        },
      }
    );
    const data = await res.json();
    if (res.ok) {
      return data;
    } else {
      throw new Error(data);
    }
  }

  function handleOnLoad() {
    promise = getAllArticles();
  }
</script>

<div on:load={handleOnLoad} class="container mx-auto p-4">
  <div class="grid md:grid-cols-1 sm:grid-cols-1 justify-items-center">
    {#await promise}
      <div>
        <h1 class="text-2xl font-bold" style="color: #ECEFF4;">Cargando el contenido...</h1>
      </div>
    {:then articles}
      {#each articles as { id, name, content, type, duration, link }, i}
        <Card name={name} content={content} type={type} duration={duration} link={link}/>
      {/each}
    {:catch error}
    <div>
      <h1 class="text-2xl font-bold" style="color: #ECEFF4;">Ocurrio un error en el servidor :(</h1>
    </div>
    {/await}
  </div>
</div>
