<template>
  <header :class="$style.header">
    <nav :class="$style.navigation">
      <Swicth />
    </nav>
  </header>
</template>

<script>
import Swicth from '~/components/Switch/Switch.vue'
export default ({
  name: "Navigation",
  components: {
    Swicth,
  }
})
</script>


<style module lang="scss">
.header{
  display: flex;
  justify-content: center;
  padding: var(--content-vertical-spacing) var(--content-horizontal-spacing);
}
.navigation {
  width: 100%;
  max-width: var(--max-content-width);
}
</style>