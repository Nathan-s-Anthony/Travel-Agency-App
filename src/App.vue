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
</script>

<template>

  <header>
    <HeaderNavigation />
  </header>

  <main>
    <TabWrapper>
      <TabItems title="DISCOVER">
        <TripSlider />
        <FeaturedPlaces />
        <PlacesVist />
        <PlacesList />
      </TabItems>
      <TabItems title="ACTIVITIES">Activities content</TabItems>
    </TabWrapper>
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
