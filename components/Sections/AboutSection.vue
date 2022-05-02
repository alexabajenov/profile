<template>
  <div :class="$style.container">
    <div :class="$style.topImageContainer">
      <div :class="$style.textContainer">
        <p>who am I ?</p>
        <p :class="$style.textMain">About <span>me</span></p>
      </div>
    </div>
    <div :class="$style.aboutContainer">
      <div></div>
      <div></div>
      <div :class="$style.imageWrapper">
        <img src="~/assets/img/my-photo.jpg" alt="about-image">
      </div>
    </div>
    <div></div>
  </div>
</template>

<style module lang="scss">
  .container {
    background-color: var(--layout-color-1);
    .topImageContainer {
      position: relative;
      top: -2px;
      background-image: url('~/assets/img/back-top.png');
      background-position: top;
      background-size: cover;
      height: 220px;
      .textContainer {
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
        align-content: flex-end;
        height: 100%;
        max-width: var(--max-content-width);
        padding: 0 var(--content-horizontal-spacing);
        margin: 0 auto;
        > p:first-child {
          margin-bottom: var(--spacing-xl);
        }
        .textMain {
          font-size: var(--text-xl);
          font-weight: 600;
          span {
            color: var(--second-text-color);
          }
        }
      }
    }
    .aboutContainer {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 40px;
      width: 100%;
      max-width: var(--max-content-width);
      padding: 0 var(--content-horizontal-spacing);
      .imageWrapper {
        border-radius: 48px;
        background-color: var(--layout-color-2);
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
    }
  }
</style>