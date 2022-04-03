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
      <div class="featured-tile-additional">
        <div class="featured-tile-weather">
          <IconSunnyAlt />
          <p>{{ featured.meta.weather.conditions }}</p>
          <p>{{ featured.meta.weather.temperature }}</p>
        </div>
        <div class="featured-tile-likes">
          <div>
            <IconLove /> <sup>{{ featured.meta.likes }}K</sup>
          </div>
        </div>
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
import IconSunnyAlt from "./icons/IconSunnyAlt.vue";
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
      })
      .catch((error) => {
        console.log(error);
      });
  },
  components: { IconMore, IconSunny, IconSaved, IconLove, IconSunnyAlt },
};
</script>
