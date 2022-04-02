<template>
<div class="tabs-wrapper">
  <div class="tabs">
    <ul class="tabs-header">
      <li
        v-for="title in tabTitles"
        :key="title"
        @click="selectedTitle = title"
        :class="{selected : title == selectedTitle}"
      >
        {{ title }}
      </li>
    </ul>

    <slot></slot>
  </div>
  </div>
</template>
<script>
import { ref, provide } from "vue";
export default {
  setup(props, { slots }) {
    const tabTitles = ref(slots.default().map((tab) => tab.props.title));
    const selectedTitle = ref(tabTitles.value[0]);

    provide("selectedTitle", selectedTitle);
    return {
      tabTitles,
      selectedTitle,
    };
  },
};
</script>
<style scoped lang="scss">
@import "../assets/scss/components/tabs.scss";
</style>