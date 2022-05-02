<template>
  <button :class="$style.button">
    <span>{{ text }}</span>
    <span><slot /></span>
  </button>
</template>

<script>
export default ({
  props: {
    text: {
      type: String,
      requred: true,
    }
  },
})
</script>


<style module lang="scss">
  .button {
    display: flex;
    align-items: center;
    gap: .8rem;
    padding: 0.6rem 1.5rem;
    border: none;
    border-radius: 46px;
    font-size: var(--text-m);
    background-color: var(--layout-color-2);
    color: var(--white);
    cursor: pointer;
    transition: .3s;
    &:hover {
      box-shadow: var(--box-shadow);
    }
  }
</style>
