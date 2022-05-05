<script>
  import { Router, Route } from "svelte-navigator";
  import NavBar from "./NavBar.svelte";
  import Home from "./Home.svelte";
  import Tutorials from "./Tutorials.svelte";
</script>

<Router>
  <NavBar />
  <main>
    <Route path="/">
      <Home />
    </Route>
    <Route path="tutoriales">
      <Tutorials />
    </Route>
  </main>
</Router>
