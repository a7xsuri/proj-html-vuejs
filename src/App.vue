<template>
  <div id="app" class="container-fluid">
    <header-app/>
    <div class="container">
      <main-app/>
    </div>
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
@import "./style/general.scss";
@import "./style/vars.scss";
#app {
  color: #2c3e50;

  .container-fluid{
    background-color: $backgroundlightazure;
  }
}
</style>
