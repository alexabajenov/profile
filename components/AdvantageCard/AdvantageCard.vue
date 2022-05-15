<template>
  <div :class="$style.card">
    <div :class="$style.cardContainer">
      <p>{{ title }}</p>
      <div :class="$style.imgContainer">
        <img :src="image" alt="creative" :class="$style.image">
      </div>
    </div>
    <p>{{ text }}</p>
  </div>
</template>

<script>

export default ({
  props: {
    image: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      default: () => "",
    },
    text: {
      type: String,
      default: () => "",
    },
  },
})
</script>

<style module lang="scss">
.card {
  width: 235px;
  min-width: 150px;
  .imgContainer {
    width: 100%;
  }
  .image {
    width: 100%;
    height: auto;
  }
  .cardContainer {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    padding: 45px 45px 20px 45px;
    border: 1px solid var(--second-text-color);
    border-radius: 12px;
    text-align: center;
    margin-bottom: var(--spacing-2xl);
    > p {
      font-size: 26px;
      font-weight: 500;
    }
  }
  @media (max-width: 991px) {
    width: 180px;
  }
  @media (max-width: 575px) {
    max-width: 260px;
    width: 100%;
  }
}
</style>
