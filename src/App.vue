<template>
  <v-app>
    <app-navigation></app-navigation>
    <v-content transition="slide-x-transition">
      <router-view></router-view>
      <div id="filigrane">
        <v-img src="@/assets/logo.png"></v-img>
      </div>
    </v-content>
  </v-app>
</template>

<script>
import AppNavigation from "@/components/AppNavigation";
export default {
  name: "App",

  components: {
    AppNavigation
  },

  data: () => ({
    //
  })
};
</script>
<style scoped>
#filigrane {
  position: absolute;
  width: 30%;
  right: 0px;
  bottom: 0px;
  opacity: 0.1;
}
</style>
