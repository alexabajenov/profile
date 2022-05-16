<template>
  <section :class="$style.section">
    <div :class="$style.container">
      <div :class="$style.header">
        <p>what my latest projects?</p>
        <h2 :class="$style.title">My <span>Projects</span></h2>
      </div>
      <div :class="$style.mainContainer">
        <div :class="$style.imageContainer">
          <img src="~/assets/img/franzeluta.png" alt="project">
        </div>
        <div :class="$style.imageBottomContainer">
           <img src="~/assets/img/arrow-down.svg" alt="arrow">
        </div>
        <div :class="$style.imageCollectionsContainer">
          <div v-for="item in images" :key="item" :class="$style.image">
            <img :src="require(`~/assets/img/${item}`)" alt="arrow">
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>

export default ({
  data() {
    return {
      images: ["proj-one.png", "proj-three.png", "proj-two.png"],
    }
  }
})
</script>

<style module lang="scss">
.section {
  width: 100%;
  .container {
    width: 100%;
    max-width: var(--max-content-width);
    margin: 0 auto;
    padding: 0 var(--content-horizontal-spacing);
    .header {
      > p {
        margin-bottom: var(--spacing-2xl);
      }
      > h2 {
        font-size: var(--text-xl);
        margin-bottom: var(--spacing-xl);
        span {
          color: var(--second-text-color);
        }
      }
    }
    .mainContainer {
      display: flex;
      flex-direction: column;
      align-items: center;
      width: 100%;
      justify-content: center;
      .imageContainer, 
      .imageBottomContainer  {
        display: flex;
        width: 70%;
        > img {
          width: 100%;
          height: auto;
        }
      }
      .imageBottomContainer {
        padding: var(--spacing-2xl) 0;
        height: 110px;
      }
      .imageCollectionsContainer {
        display: flex;
        width: 100%;
        gap: var(--spacing-2xl);
        .image {
          width: 100%;
          > img {
            width: 100%;
            height: auto;
          }
        }
      }
    }
  }
}
</style>
