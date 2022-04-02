<script setup>
import HeaderNavigationItemVue from "./HeaderNavigationItem.vue";
import IconNavigationMenu from "./icons/IconNavigationMenu.vue";
import IconActivity from "./icons/IconActivity.vue";
import IconSearch from "./icons/IconSearch.vue";
</script>
<template>
  <nav>
    <div class="navigation-menu">
      <HeaderNavigationItemVue>
        <template #icon>
          <IconNavigationMenu />
        </template>
      </HeaderNavigationItemVue>
    </div>

    <div class="heading-container">
      <h3>Explore</h3>
    </div>
    <div class="icon-container">
      <HeaderNavigationItemVue>
        <template #icon>
          <IconActivity class="notification-icon" />
        </template>
      </HeaderNavigationItemVue>
      <HeaderNavigationItemVue>
        <template #icon>
          <IconSearch />
        </template>
      </HeaderNavigationItemVue>
    </div>
  </nav>
</template>
<style scoped lang="scss">
@import "../assets/scss/components/header.scss";
</style>
