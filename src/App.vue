<template>
  <div id="app">
    <SplashView />
    <About />
  </div>
</template>

<script>
import SplashView from "./components/SplashView.vue";
import About from "./components/About.vue";

export default {
  name: "App",
  components: {
    SplashView,
    About,
  },
};
</script>

<style>
html {
  max-width: 100%;
  overflow-x: hidden;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 10px;
}
a {
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
body {
  margin: 0;
}
.test {
  height: 70vh;
}
.flex {
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
}
</style>
