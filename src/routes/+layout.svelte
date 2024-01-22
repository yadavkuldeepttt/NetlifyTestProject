<script>
  import "./styles.css";
  let show = true;
  setTimeout(() => (show = false));
</script>

<div class="app">
  <main>
    <slot />
  </main>
</div>

<style>
</style>
