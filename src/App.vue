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
  font-size: 10px;
}
body {
  margin: 0;
  /* background-color: purple; */
}
.test {
  height: 1000px;
}
.flex {
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
}
</style>
