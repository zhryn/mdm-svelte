<script>
  import { Button } from "sveltestrap";
  import * as animateScroll from "svelte-scrollto";

  export let leadIn = "";
  export let heading = "";
  export let btnText = "";
  export let btnDestination = "";

  const handleScroll = el => {
    animateScroll.scrollTo({ element: el });
  };
</script>

<header class="masthead">
  <div class="container">
    <div class="intro-text">
      <div class="intro-lead-in">{leadIn}</div>
      <div class="intro-heading text-uppercase">{heading}</div>
      <Button
        class="btn btn-primary btn-lg text-uppercase"
        on:click={() => handleScroll(btnDestination)}>
        {btnText}
      </Button>
    </div>
  </div>
</header>
