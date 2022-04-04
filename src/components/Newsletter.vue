<template>
  <div class="newsletter-container">
    <div class="newsletter-content">
      <h3>Newsletter</h3>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque.
      </p>
      <form action="#">
        <input type="email" placeholder="Email Address" />
        <button type="submit"><IconSendIcon /></button>
      </form>
    </div>
  </div>
</template>
<style scoped lang="scss">
@import "../assets/scss/components/newsletter.scss";

</style>
<script>
import IconSendIcon from "./icons/IconSendIcon.vue";
import AppButtons from "./AppButtons.vue";
export default {
  name: "App",
  components: {
  IconSendIcon,
  },
};
</script>
