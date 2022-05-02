<template>
  <div>
    <Navigation />
    <main :class="$style.main">
      <Nuxt />
    </main>
    <footer></footer>
  </div>
</template>

<script>
import Navigation from '~/components/Navigation/Navigation.vue'
export default {
  components: {
    Navigation
  },
}
</script>

<style module lang="scss">
  .main {
    position: relative;
  }
</style>
