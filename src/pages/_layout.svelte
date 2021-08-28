<script>
  import Navbar from "../components/Navbar.svelte";
</script>
<Navbar />
<div class="slots-styles">
    <slot />
</div>
<style>
    .slots-styles {
        position: absolute;
        top: 0;
        width: 100%;
        height: 100%;
        padding: 0;
        margin: 0;
        z-index: 0;
    }
</style>
