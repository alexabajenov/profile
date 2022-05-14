<template>
  <div :class="$style.container">
    <p :class="$style.text">what my advantages?</p>
    <h2 :class="$style.header">My <span>Advantages</span></h2>
  </div>
</template>

<script>

export default ({
  // 
})
</script>

<style module lang="scss">
.container {
  padding: 60px;
  .text {
    position: relative;
    top: -1rem;
  }
  .header {
    > span {
      color: var(--second-text-color);
    }
  }
}
</style>
