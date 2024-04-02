<script lang="ts">
  import Choices from './lib/Choices.svelte';
</script>

<main class="container">
  <h1>photo-slap</h1>
  <img src="/photo-slap.svg" class="logo slap" alt="Slap Logo" />
  <p>
    welcome to the show
  </p>

  <div class="row">
    <Choices />
  </div>


</main>

<style>
  .logo.slap {
    filter: drop-shadow(0 0 2em #747bff);
  }
</style>