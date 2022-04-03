<template>
  <div class="trip-container">
    <h1>An exquisite trip you'll rave about to your friends</h1>

    <button @click="prev">&#8226;</button>
    <img :src="image" />

    <button @click="next">&#8226;</button>
  </div>
</template>
<script>
const images = [
 "./assets/images/view-of-ocean-from-plane-window.png",
];

export default {
  name: "App",
  data() {
    return { index: 0, image: images[0] };
  },
  methods: {
    next() {
      this.index = (this.index + 1) % images.length;
      this.image = images[this.index];
    },
    prev() {
      this.index = (this.index - 1) % images.length;
      this.image = images[this.index];
    },
  },
};
</script>
