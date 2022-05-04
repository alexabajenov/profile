<template>
  <header :class="$style.header">
    <nav :class="$style.navigation">
      <SwicthButton />
    </nav>
  </header>
</template>

<script>
import SwicthButton from '~/components/SwicthButton/SwicthButton.vue'
export default ({
  name: "Navigation",
  components: {
    SwicthButton,
  }
})
</script>


<style module lang="scss">
.header{
  position: sticky;
  top: 0;
  left: 0;
  display: flex;
  justify-content: center;
  padding: var(--content-vertical-spacing) var(--content-horizontal-spacing);
  background-image: var(--header-gradient);
  z-index: 10;
}
.navigation {
  width: 100%;
  max-width: var(--max-content-width);
}
</style>