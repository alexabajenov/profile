<template>
  <div>
    <Navigation />
    <main>
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

<style module>

</style>
