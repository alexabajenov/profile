<template>
  <section :class="$style.section">
    <div :class="$style.container">Hello</div>
  </section>
</template>

<script>
export default {
  name: 'ProfilePage',
}
</script>

<style module lang="scss">
  .section {
    padding: 0 var(--content-horizontal-spacing);
    width: 100%;
    .container {
      width: 100%;
      max-width: var(--max-content-width);
       margin: 0 auto;
    }
  }
</style>
