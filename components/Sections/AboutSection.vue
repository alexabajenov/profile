<template>
  <section>
    <div :class="$style.container">
      <div :class="$style.topImageContainer">
        <div :class="$style.textContainer">
          <p>who am I ?</p>
          <p :class="$style.textMain">About <span>me</span></p>
        </div>
      </div>
      <div :class="$style.aboutContainer">
        <div :class="$style.aboutWrapper">
          <div>
            <DescriptionList :data="textData" />
          </div>
          <div :class="$style.centerWrapper">
            <img src="~/assets/img/arrow-snake.png" alt="arrow-img" />
          </div>
          <div :class="$style.imageWrapper">
            <img src="~/assets/img/my-photo.jpg" alt="about-image" />
          </div>
        </div>
      </div>
    </div>
    <div :class="$style.footerImage"></div>
  </section>
</template>

<script>
import { textData } from '~/data/text-data'
import DescriptionList from '~/components/DescriptionList/DescriptionList'

export default {
  components: {
    DescriptionList,
  },
  data() {
    return {
      textData,
    }
  },
}
</script>

<style module lang="scss">
.container {
  margin: 0 auto;
  background-color: var(--layout-color-1);
  padding-bottom: 1rem;
  max-width: var(--max-content-width);
  .topImageContainer {
    position: relative;
    top: -2px;
    background-image: url('~/assets/img/back-top.png');
    background-position: top;
    background-size: cover;
    height: 240px;
    width: 100%;
    padding: 0 var(--content-horizontal-spacing);
    margin-bottom: var(--spacing-6xl);
    .textContainer {
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      align-content: flex-end;
      height: 100%;
      max-width: var(--max-content-width);
      margin: 0 auto;
      > p:first-child {
        margin-bottom: var(--spacing-xl);
      }
      .textMain {
        position: relative;
        font-size: var(--text-xl);
        font-weight: 600;
        font-family: 'Montserrat Alternates', 'sans-serif';
        &::before {
          content: '';
          position: absolute;
          bottom: 0;
          left: 0;
          width: 3.4rem;
          height: 3px;
          background-color: var(--second-text-color);
        }
        span {
          color: var(--second-text-color);
        }
      }
    }
  }
  .aboutContainer {
    width: 100%;
    padding: 0 var(--content-horizontal-spacing);
    .aboutWrapper {
      display: grid;
      grid-template-columns: minmax(200px, 242px) auto minmax(200px, 350px);
      justify-items: center;
      gap: 40px;
      align-items: center;
      max-width: var(--max-content-width);
      .imageWrapper {
        border-radius: 48px;
        background-color: var(--layout-color-2);
        max-width: 350px;
        img {
          position: relative;
          left: -16px;
          top: 16px;
          border-radius: 48px;
          overflow: hidden;
          width: 100%;
          height: auto;
        }
      }
      .centerWrapper {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        padding: 0 1rem;
        max-width: 250px;
        img {
          width: 100%;
          height: auto;
        }
      }
      @media (max-width: 991px) {
        grid-template-columns: 1fr;
        grid-template-rows: auto;
      }
    }
  }
}
.footerImage {
  width: 100%;
  height: 160px;
  max-width: var(--max-content-width);
  background-image: url('~/assets/img/back-bottom.png');
  background-position: top;
  background-size: cover;
  position: relative;
  top: -2px;
  margin: 0 auto;
}
</style>
