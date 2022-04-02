<template>
  <div class="featured-container">
    <div class="featured">
      <h2>Featured</h2>
      <AppButtons />
    </div>
    <div class="featured-tiles-container">
    <div class="featured-tile-items">test</div>
    <div class="featured-tile-items">test</div>
     <div class="featured-tile-items">test</div>
    <div class="featured-tile-items">test</div>
    </div>
  </div>
</template>
<style scoped lang="scss">
@import "../assets/scss/components/featuredplaces.scss";
</style>
<script>
import AppButtons from "./AppButtons.vue";
export default {
  name: "App",
  components: {
    AppButtons,
  },
};
</script>
