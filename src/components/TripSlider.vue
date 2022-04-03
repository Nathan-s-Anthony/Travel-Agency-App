<template>
  <div class="trip-container">
    <div class="trip-slider-trip-info">
      <span>$967</span>
      <span>&#8226;</span>
      <span>Tenessey</span>
    </div>
    <h1>An exquisite trip you'll rave about to your friends</h1>

    <button>Get Access <span ><IconArrow /></span></button>
    <div class="trip-slider-navigation">
      <div class="navigation-dot"></div>
      <div class="navigation-dot"></div>
    </div>
  </div>
</template>
<style scoped lang="scss">
@import "../assets/scss/components/tripSlider.scss";
</style>
<script>
import IconArrow from "./icons/IconArrow.vue";
import AppButtons from "./AppButtons.vue";
export default {
  name: "App",
  components: {
    AppButtons,
    IconArrow
  },
};
</script>
