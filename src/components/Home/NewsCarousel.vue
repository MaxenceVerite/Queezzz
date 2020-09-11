<template>
  <div>
    <v-carousel v-model="model">
      <v-carousel-item v-for="(item) in news" :key="item"></v-carousel-item>
    </v-carousel>
  </div>
</template>
<script>
export default {
  name: "NewsCarousel",

  components: {},

  data() {
    return {
      appTitle: "Queezzz",
      drawer: false,
      news: [
        { img: "https://picsum.photos/200/300", desc: "Menu" },
        { img: "https://picsum.photos/200/300", desc: "Sign In" },
        { img: "https://picsum.photos/200/300", desc: "Join" }
      ]
    };
  }
};
</script>
<style>
</style>