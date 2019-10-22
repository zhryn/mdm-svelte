<script>
  import { Collapse, Navbar, NavbarToggler, NavbarBrand } from "sveltestrap";
  import { isNavbarOpen } from "../store.js";

  export let id = "";

  let scrollY = 0;
  let isOpen = false;

  const unsubscribe = isNavbarOpen.subscribe(v => {
    isOpen = v;
  });

  const toggle = () => {
    isNavbarOpen.set(!isOpen);
  };

  const handleResponsive = e => {
    isNavbarOpen.set(e.detail.isOpen);
  };
</script>

<svelte:window bind:scrollY />

<Navbar
  {id}
  dark
  expand="lg"
  fixed="top"
  class={scrollY > 100 ? 'navbar-shrink' : ''}>
  <div class="container">
    <NavbarBrand href="#" class="mr-auto">
      <slot name="brand" />
    </NavbarBrand>
    <NavbarToggler on:click={toggle} className="mr-2">
      Menu
      <i class="fas fa-bars" />
    </NavbarToggler>
    <Collapse {isOpen} navbar expand="lg" on:update={handleResponsive}>
      <slot />
    </Collapse>
  </div>
</Navbar>
