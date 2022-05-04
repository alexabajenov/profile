<template>
  <div :class="$style.container">
    <div v-for="(item, index) in data" :key="index" :class="$style.card">
      <div :class="$style.digit">{{ index + 1 }}</div>
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
  gap: var(--spacing-m);
  .card {
    display: grid;
    grid-template-columns: 2.5rem auto;
    align-items: center;
    width: 100%;
    .digit {
      font-size: var(--text-xl);
      color: var(--omit-text-color);
    }
    .text {
      padding-left: var(--spacing-2xl);
      border-left: 3px solid var(--layout-color-2);
    }
  }
}

</style>