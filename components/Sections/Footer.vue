<template>
  <footer :class="$style.footer">
    <div :class="$style.container">
      <div :class="$style.header">
        <h2>Contact <span>me</span></h2>
        <div :class="$style.imageContainer">
          <img src="~/assets/img/cuate.png" alt="cuate">
        </div>
      </div>
      <div></div>
      <div></div>
    </div>
  </footer>
</template>

<script>
export default ({
  //
})
</script>

<style module lang="scss">
.footer {
  width: 100%;
  .container {
    width: 100%;
    max-width: var(--max-content-width);
    margin: 0 auto;
    padding: 50px var(--content-horizontal-spacing) 32px var(--content-horizontal-spacing);
    background-color: var(--layout-color-1);
    display: flex;
    flex-direction: column;
    align-items: center;
    .header {
      display: flex;
      justify-content: space-between;
      width: 100%;
      > h2 {
        font-size: var(--text-xl);
        white-space: nowrap;
        span {
          color: var(--second-text-color);
        }
      }
      .imageContainer {
        display: flex;
        > img {
          width: 100%;
          height: auto;
        }
      }
    }
  }
}
</style>