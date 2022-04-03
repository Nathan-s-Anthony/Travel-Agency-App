<template>
  <div class="featured-tiles-container">
    <div
      class="featured-tile-items"
      v-for="featured in featured"
      :key="featured.title"
    >
      <div class="featured-tile-img">
        <img :srcset="featured.images['145']" />
      </div>
      <div class="featured-tile-info">
        <h5>{{ featured.title }}</h5>
        <IconMore />
      </div>
      <div class="featured-tile-more">
        <p>${{ featured.price }}</p>
        <span></span>
        <p>{{ featured.location }}</p>
       
      </div>
      <div class="test">
        {{ featured.meta.weather.temperature }}
      </div>
    </div>
  </div>
</template>
<style lang="scss">
@import "../assets/scss/components/featuredplaces.scss";
</style>
<script>
import IconMore from "./icons/IconMore.vue";
import IconSunny from "./icons/IconSunny.vue";
import IconSaved from "./icons/IconSaved.vue";
import IconLove from "./icons/IconLove.vue";
import axios from "axios";

export default {
  data() {
    return {
      featured: [],
    };
  },
  mounted() {
    //fetching the api data from the server
    axios
      .get("https://www.afrihost.com/resources/fedev/places.json")
      .then((response) => {
        this.featured = response.data.featured;
      });
  },
  components: { IconMore, IconSunny, IconSaved, IconLove },
};
</script>
