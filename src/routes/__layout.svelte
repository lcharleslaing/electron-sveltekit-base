<script>
  import "../app.scss";
  import SideBar from "$lib/components/SideBar.svelte";
</script>

<SideBar />

<div class="main">
  <slot />
</div>
