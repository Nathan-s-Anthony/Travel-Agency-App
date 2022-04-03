<template>
  <div class="featured-tiles-container">
      <div class="featured-tile-items" v-for="featured in featured" :key="featured.title">
    
    <h5>{{ featured.title }} {{ featured.price }}</h5>
    <p>{{ featured.title }}</p>
  </div>
  </div>
 
</template>
<style  lang="scss">
@import "../assets/scss/components/featuredplaces.scss";
</style>
<script>
import axios from "axios";

export default {
  data() {
    return {
      featured: [],
    };
  },
  mounted() {
 
    axios
      .get("https://www.afrihost.com/resources/fedev/places.json")
      .then((response) => {
        this.featured = response.data.featured;
      });
  },
};

</script>
