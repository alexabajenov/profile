<template>
  <div :class="$style.container">
    <p :class="$style.text">what my advantages?</p>
    <h2 :class="$style.header">My <span>Advantages</span></h2>
    <div :class="$style.cardsContainer">
      <template v-for="item in list">
        <AdvantageCard 
          :image="require(`~/assets/img/${item.img}`)" 
          :title="item.title"
          :text="item.text"
          :key="item.title"
        />
      </template>
    </div>
  </div>
</template>

<script>
import AdvantageCard from "~/components/AdvantageCard/AdvantageCard.vue"
export default ({
  components: {
    AdvantageCard,
  },
  data() {
    return {
      list: [
        { img: "creative.svg", title: "Creativity", text: "Сreative projects are the main part of my work"},
        { img: "arrow-1.svg", title: "Quality", text: "My work is always done qualitatively"},
        { img: "speed.svg", title: "Rapidity", text: "I do my job quickly and correctly"},
        { img: "sociable.svg", title: "Sociable", text: "I am very sociable and will find a common language with everyone"},
      ]
    }
  }
  // 
})
</script>

<style module lang="scss">
.container {
  padding: 60px var(--content-horizontal-spacing);
  .text {
    position: relative;
    top: -1rem;
  }
  .header {
    position: relative;
    font-size: var(--text-xl);
    white-space: nowrap;
    > span {
      color: var(--second-text-color);
    }
    margin-bottom: 120px;
    &::before {
      position: absolute;
      content: "";
      bottom: -0.5rem;
      height: 3px;
      width: 3.4rem;
      background-color: var(--second-text-color);
    }
  }
  .cardsContainer {
    width: 100%;
    display: flex;
    justify-content: space-between;
    gap: var(--spacing-m);
    @media (max-width: 991px) {
      flex-wrap: wrap;
      gap: var(--spacing-2xl);
      justify-content: center;
    }
    @media (max-width: 575px) {
      flex-direction: column;
      gap: var(--spacing-2xl);
      justify-content: center;
    }
  }
}
</style>
