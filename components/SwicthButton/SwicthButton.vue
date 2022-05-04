<template>
  <div :class="[$style.switch, {[$style.active]: state}]" @click="handleClick"></div>
</template>

<script>
export default ({
  data() {
    return {
      state: false,
    }
  },
  methods: {
    handleClick () {
      this.state = !this.state
      console.log("Click:", this.state)
    }
  },
})
</script>

<style module lang="scss">
.switch {
  display: flex;
  align-items: center;
  position: relative;
  width: 50px;
  height: 30px;
  border: 3px solid var(--black);
  border-radius: 30px;
  transition: .3s;
  &::before {
    position: absolute;
    content: "";
    border-radius: 50%;
    height: 15px;
    width: 15px;
    left: 10px;
    background-color: var(--black);
    transition: .3s;
  }
  &.active::before {
    transform: translateX(15px);
  }
  &.active {
    background-color: var(--layout-color-2);
  }
}
</style>