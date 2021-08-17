<script>
  import { Router, Route } from "svelte-routing";
  import NavLink from "./components/NavLink.svelte";
  import Home from "./routes/Home.svelte";
  import About from "./routes/About.svelte";
  import Blog from "./routes/Blog.svelte";
  import BlogId from "./routes/BlogId.svelte";
  import NotFound from "./routes/NotFound.svelte";

  export let url = "";
</script>

<Router url="{url}">
  <nav>
    <NavLink to="/">Home</NavLink>
    <NavLink to="about">About</NavLink>
    <NavLink to="blog">Blog</NavLink>
  </nav>
  <div>
    <Route component="{NotFound}" />
    <Route path="about" component="{About}" />
    <Route path="blog/" component="{Blog}" />
    <Route path="blog/:id" component="{BlogId}" let:params />
    <Route path="/" component="{Home}" />
  </div>
</Router>
