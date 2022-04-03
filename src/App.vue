<script setup>
import HeaderNavigation from "./components/HeaderNavigation.vue";
import TripSlider from "./components/TripSlider.vue";
import TabWrapper from "./components/TabWrapper.vue";
import TabItems from "./components/TabItems.vue";
import PlacesVist from "./components/PlacesVist.vue";
import FeaturedPlaces from "./components/FeaturedPlaces.vue";
import PlacesList from "./components/PlacesList.vue";
import FooterNavigation from "./components/FooterNavigation.vue";
import TripSliderItems from "./components/TripSliderItems.vue";
import FeaturedPlacesItems from "./components/FeaturedPlacesItems.vue";
import Newsletter from "./components/Newsletter.vue";

</script>

<template>

  <header>
    <HeaderNavigation />
  </header>

  <main>
    <TabWrapper>
      <TabItems title="DISCOVER">
        <TripSlider />
        <!-- <TripSliderItems /> -->
        <FeaturedPlaces />
        <FeaturedPlacesItems />
        <PlacesVist />
        <PlacesList />
      </TabItems>
      <TabItems title="ACTIVITIES">Activities content</TabItems>
    </TabWrapper>
    <Newsletter />
  </main>
  <footer>
<FooterNavigation />
  </footer>

</template>

<style lang="scss">
#app {
  max-width: 425px;
  margin: 0 auto;
  background: $appBg;
}
</style>
