<template>
  <div :class="$style.container">
    <div v-for="(item, index) in data" :key="index" :class="$style.card">
      <div :class="$style.digit">0{{ index + 1 }}</div>
      <div :class="$style.text">{{ item }}</div>
    </div>
  </div>
</template>

<script>

export default ({
  props: {
    data: {
      required: true,
    }
  }
})
</script>


<style module lang="scss">
.container {
  width: 100%;
  display: grid;
  grid-template-rows: auto;
  gap: var(--spacing-xxl);
  .card {
    border-left: 3px solid var(--layout-color-2);
    position: relative;
    .digit {
      position: absolute;
      left: -0.65em;
      top: -1.45em;
      font-size: var(--text-s);
      color: var(--omit-text-color);
      transform: rotate(-90deg);
    }
    .text {
      display: flex;
      width: 100%;
      align-items: center;
      padding-left: var(--spacing-2xl);
      height: 100%;
    }
  }
}

</style>