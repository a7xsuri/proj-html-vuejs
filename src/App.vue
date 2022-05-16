<template>
  <div id="app" class="container">
    <header-app/>
    <main-app/>
    <footer-app/>
  </div>
</template>

<script>
import HeaderApp from "./components/HeaderApp.vue";
import MainApp from "./components/MainApp.vue";
import FooterApp from "./components/FooterApp.vue";


export default {
  name: 'App',
  components: {
    HeaderApp,
    MainApp,
    FooterApp
  }
}
</script>

<style lang="scss">
#app {

  color: #2c3e50;
}
</style>
