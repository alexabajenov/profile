<template>
  <section :class="$style.section">
    <div :class="$style.container">
      <div :class="$style.col">
        <p :class="$style.title">Hello</p>
        <h1 :class="$style.user">I’m<br>Alexandra Bajenova</h1>
        <p :class="$style.info">I am a web designer</p>
        <p :class="$style.description">I will make your websites modern , creative and adaptive for all devices</p>
        <Button text="contact me">
          <img src="~/assets/img/arrow.svg" alt="arrow">
        </Button>
      </div>
      <div :class="[$style.col, $style.image]">
        <img src="~/assets/img/header-image.png" alt="main-image">
      </div>
    </div>
  </section>
</template>

<script>
import Button from "~/components/Button/Button.vue"
export default {
  name: 'UserSection',
  components: {
    Button,
  }
}
</script>

<style module lang="scss">
  .section {
    padding: 0 var(--content-horizontal-spacing);
    width: 100%;
    .container {
      display: flex;
      width: 100%;
      max-width: var(--max-content-width);
      margin: 0 auto;
      .col {
        width: 50%;
        .title, .user {
          margin-bottom: var(--spacing-5xl);
        }
        .info {
          color: var(--second-text-color);
          font-size: var(--text-l);
          margin-bottom: var(--spacing-xs);
        }
        .description {
          max-width: 320px;
          margin-bottom: var(--spacing-5xl);
        }
      }
      .image {
        display: flex;
        justify-content: center;
        align-items: center;
        img {
          width: 100%;
          height: auto;
        }
      }
    }
  }
</style>