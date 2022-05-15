<template>
  <div :class="$style.container">
    <div :class="$style.topWave" :style="{ backgroundImage: `url('${vaweTopImg}')` }"></div>
    <div :class="$style.mainContainer">
      <div :class="$style.header">
        <p>which programs do i know ?</p>
        <h2 :class="$style.title">My <span>Experiences</span></h2>
      </div>
      <div :class="$style.cardsContainer">
        <template v-for="item in list">
          <ExperienceCrad :title="item.title" :image="item.image" :key="item.title"/>
        </template> 
      </div>
    </div>
    <div :class="$style.bottomWave" :style="{ backgroundImage: `url('${vaweBottomImg}')` }"></div>
  </div>
</template>

<script>

export default ({
  data() {
    return {
      vaweTopImg: (require('~/assets/img/wave-top.png')),
      vaweBottomImg: (require('~/assets/img/wave-bottom.png')),
      list: [
        { title: "Figma", image: "figma.svg" },
        { title: "Tilda", image: "tilda.svg" },
        { title: "Photoshop", image: "photoshop.svg" },
        { title: "Illustrator", image: "illustrator.svg" },
      ],
    }
  }
})
</script>

<style module lang="scss">
.container {
  .topWave {
    width: 100%;
    height: 100px;
    background-size: cover;
    background-position: top;
  }
  .mainContainer {
    width: 100%;
    display: flex;
    flex-direction: column;
    background-color: var(--layout-color-1);
    padding: 60px var(--content-horizontal-spacing);
    .header {
      text-align: right;
      margin-bottom: 110px;
      > h2 {
        position: relative;
        font-size: var(--text-xl);
        white-space: nowrap;
        &::before {
          position: absolute;
          content: "";
          bottom: -0.5rem;
          height: 3px;
          width: 3.4rem;
          background-color: var(--second-text-color);
        }
        > span {
          color: var(--second-text-color);
        }
      }
    }
    .cardsContainer {
      display: flex;
      justify-content: space-between;
      gap: var(--spacing-m);
      @media (max-width: 991px) {
        flex-wrap: wrap;
        justify-content: center;
        gap: var(--spacing-2xl);
      }
      @media (max-width: 575px) {
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: var(--spacing-2xl);
      }
    }
  }
  .bottomWave {
    width: 100%;
    height: 155px;
    background-size: cover;
    background-position: top;
  }
}

</style>
