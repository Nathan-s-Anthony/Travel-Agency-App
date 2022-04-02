<script setup>
import FooterNavigationItems from "./FooterNavigationItems.vue";
import IconTravel from "./icons/IconTravel.vue";
import IconExplore from "./icons/IconExplore.vue";
import IconSaved from "./icons/IconSaved.vue";
import IconChat from "./icons/IconChat.vue";
import IconProfile from "./icons/IconProfile.vue";
</script>

<template>
  <div class="footer-navigation">
    <div class="footer-navigation-items">
      <FooterNavigationItems>
        <template #icon>
          <IconTravel />
        </template>
      </FooterNavigationItems>
      <FooterNavigationItems>
        <template #icon>
          <IconExplore />
        </template>
      </FooterNavigationItems>
      <FooterNavigationItems>
        <template #icon>
          <IconSaved />
        </template>
      </FooterNavigationItems>
      <FooterNavigationItems>
        <template #icon>
          <IconChat />
        </template>
      </FooterNavigationItems>
      <FooterNavigationItems>
        <template #icon>
          <IconProfile />
        </template>
      </FooterNavigationItems>

    </div>
          <div class="tasbar"></div>
  </div>
</template>
<style scoped lang="scss">
@import "../assets/scss/components/footer.scss";
</style>
