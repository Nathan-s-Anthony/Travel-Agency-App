<template>
  <div class="featured-container">
    <div class="featured">
      <h2>Featured</h2>
      <AppButtons>
        <template #text>See All </template>
        <IconArrow />
      </AppButtons>
    </div>
   <div>

   </div>
  
  </div>
</template>
<style lang="scss">
@import "../assets/scss/components/featuredplaces.scss";
</style>
<script>

import IconArrow from "./icons/IconArrow.vue";
import AppButtons from "./AppButtons.vue";

export default {
  name: "App",
  components: {
    AppButtons,
    IconArrow,
  
  },
};
</script>
