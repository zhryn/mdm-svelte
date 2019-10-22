<script>
  import { NavItem, NavLink } from "sveltestrap";
  import * as animateScroll from "svelte-scrollto";
  import { isNavbarOpen } from "../store.js";


  export let text;
  export let target;

  const handleScroll = el => {
    animateScroll.scrollTo({ element: el });
    isNavbarOpen.set(false);
  };
</script>

<NavItem>
  <NavLink href="#" on:click={() => handleScroll(target)}>{text}</NavLink>
</NavItem>
