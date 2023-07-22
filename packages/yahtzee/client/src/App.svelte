<!-- App.svelte -->
<script>
  import { Router, Link, Route } from "svelte-routing";
  import Board from "./pages/Board.svelte";
  import Square from "./pages/Square.svelte";
  export let url = "/";
</script>

<Router {url}>
  <nav>
    <Link to="/">Square</Link>
    <Link to="/board">Board</Link>
  </nav>
  <div>
    <Route path="/"><Square /></Route>
    <Route path="/board"><Board /></Route>
  </div>
</Router>
