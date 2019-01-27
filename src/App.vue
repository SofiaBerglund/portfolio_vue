<template>
  <div id="app">
    <LandingPage/>
    <Router-view></Router-view>
  </div>
</template>

<script>
import LandingPage from "./components/LandingPage";

export default {
  name: "app",
  components: {
    LandingPage
  }
};
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-top: 60px;
}
@media (max-width: 450px) {
  #app {
    margin-top: 10px;
  }
}
</style>
