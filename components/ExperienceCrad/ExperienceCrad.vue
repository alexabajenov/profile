<template>
  <div :class="$style.container">
    <div :class="$style.cardContainer">
      <p>{{ title }}</p>
      <div :class="$style.imageContainer">
        <img :src="require(`~/assets/img/${image}`)" :alt="title">
      </div>
    </div>
  </div>
</template>

<script>
export default ({
  props: {
    title: {
      type: String,
      default: () => ""
    },
    image: {
      type: String,
      required: true,
    }
  }
})
</script>

<style module lang="scss">
.container {
  .cardContainer {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    border: 1px solid var(--second-text-color);
    padding: 53px;
    overflow: hidden;
    background-color: var(--white);
    box-shadow: 0 0 20px 5px #80808054;
    .imageContainer {
      width: 100px;
      height: 100px;
      position: relative;
      top: 1rem;
      > img {
        width: 100%;
        height: auto;
      }
    }
    > p {
      position: absolute;
      top: 1.5rem;
      display: flex;
      justify-content: center;
      font-size: var(--text-l);
      font-weight: 600;
    }
    @media (max-width: 1199px) {
      > p {
        font-size: var(--text-m);
      }
    }
  }
  @media (max-width: 575px) {
    max-width: 260px;
  }
}
.container:nth-child(even) > .cardContainer {
  border: 1px solid var(--layout-color-2);
}
</style>
