<script setup>
import PlacesVisitItem from "./PlacesVisitItem.vue";
import IconSunny from "./icons/IconSunny.vue";
</script>
<template>
  <div class="placesVisit-container">
    <h2>Places To Visit</h2>
    <div class="placesVisit-item">
      <div class="placesVisit-content">
        <h3>Mexico City</h3>
        <p>Morbi urna elit, porta vitae convallis non, bibendum nec diam.</p>
        <hr />
        <div class="placesVisit-weather">
            
          <PlacesVisitItem>
            <template #icon>
              <IconSunny />
            </template>
          </PlacesVisitItem>
          <div class="placesVisit-weather-info">
                <h4> 22° </h4>
          <span>Sunny</span>
     
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped lang="scss">
@import "../assets/scss/components/placesVisit.scss";
</style>
