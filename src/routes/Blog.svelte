<script>
  import { Router, Link } from "svelte-routing";
</script>

<Router>
  <h1>Blog</h1>
  <ul>
    <li><Link to="first">Today I did something cool</Link></li>
    <li><Link to="second">I did something awesome today</Link></li>
    <li><Link to="third">Did something sweet today</Link></li>
  </ul>
</Router>
