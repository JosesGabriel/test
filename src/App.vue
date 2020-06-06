<template>
  <div id="app">
    <SplashView />
  </div>
</template>

<script>
import SplashView from "./components/SplashView.vue";

export default {
  name: "App",
  components: {
    SplashView,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
