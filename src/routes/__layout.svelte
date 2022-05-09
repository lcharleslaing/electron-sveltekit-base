<script>
  import "../app.css";
  import "../app.scss";
  import SideBar from "$lib/components/SideBar.svelte";
  import Navbar from "../lib/components/Navbar.svelte";
</script>

<svelte:head>
  <title>I AM BIG2TINY</title>
</svelte:head>

<div class="">
  <Navbar />
  <slot />
</div>
