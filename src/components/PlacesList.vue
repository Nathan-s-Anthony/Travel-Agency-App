<template>
  <div class="placesList-container">
    <div class="places-tile-items" v-for="places in places" :key="places.title">
      <div class="places-tile-info">
        <h3>{{ places.title }}</h3>
        <div class="places-tile-prices">
          <span class="places-tile-price-current">${{ places.price }}</span>
          <span class="places-tile-price-per-reduced"
            >${{ places.price_reduced }}</span
          >
        </div>
        <IconMore />
        <div class="places-tile-additional">
          <IconLocation />
          <span>{{ places.location }}</span>
          <IconLove />
          <span>{{ places.meta.likes }}</span>
          <IconComment />
          <span>{{ places.meta.comments }}</span>
        </div>
      </div>

      <div class="placesList-item-img">
        <img :src="places.images['145']" :alt="places.title" />
      </div>
    </div>
  </div>
  <div class="places-view-more">
    <AppButtons>
      <template #text>All Trips<span><IconArrowAlt /></span> </template>
      
    </AppButtons>
  </div>
</template>
<style scoped lang="scss">
@import "../assets/scss/components/placesList.scss";
</style>
<script>
import IconMore from "./icons/IconMore.vue";
import IconSunny from "./icons/IconSunny.vue";
import IconSunnyAlt from "./icons/IconSunnyAlt.vue";
import IconSaved from "./icons/IconSaved.vue";
import IconLove from "./icons/IconLove.vue";
import IconLocation from "./icons/IconLocation.vue";
import IconComment from "./icons/IconComment.vue";
import AppButtons from "./AppButtons.vue";
import IconArrowAlt from "./icons/IconArrowAlt.vue";
import IconArrow from "./icons/IconArrow.vue";
import axios from "axios";

export default {
  data() {
    return {
      places: [],
    };
  },
  mounted() {
    //fetching the api data from the server

    axios
      .get("./src/places.json")
      .then((response) => {
        this.places = response.data.places.other;
      })
      .catch((error) => {
        console.log(error);
      });
  },
  components: {
    IconMore,
    IconSunny,
    IconSaved,
    IconLove,
    IconSunnyAlt,
    IconLocation,
    IconComment,
    AppButtons,
    IconArrow,
    IconArrowAlt
  },
};
</script>
