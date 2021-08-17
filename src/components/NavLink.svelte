<script>
  import { Link } from "svelte-routing";

  export let to = "";

  function getProps({ location, href, isPartiallyCurrent, isCurrent }) {
		let isActive = false;
		if (location.pathname === href) {
			isActive = true;
		} else {
			let pathname = `/${location.pathname.split("/")[1]}`;
			if (pathname === href) {
				isActive = true;
			}
		}
    if (isActive) {
      return { class: "active" };
    }
    return {};
  }
</script>

<Link to="{to}" getProps="{getProps}">
  <slot />
</Link>
