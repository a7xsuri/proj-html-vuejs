<template>
  <div id="app"> 
    <div class="container-fluid px-0 mx-0">
      <header-app/>
    </div>
    <div class="container">
      <main-app/>
    </div>
    <div class="container-fluid px-0 mx-0">
      <footer-app/>
    </div>
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
#app {
  color: #2c3e50;

  .container-fluid{
    background-color: $backgroundlightazure;
  }
}
</style>
