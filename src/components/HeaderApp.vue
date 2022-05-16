<template>
  <div id="Header">
      <img src="../assets/logo-dark.png">
      <div>
          <!-- <ul>
              <li v-for="(item, index) in Page" :key="index">{{ item.menu.Landing.SubPagesInLanding }}</li>
          </ul> -->
      </div>
  </div>
</template>

<script>
import Data from "../Data.json";

export default {
    data(){
        return{
            Page: Data,

        }
    }
}
</script>

<style lang="scss">
@import "../style/general.scss";
img {
    width: 10%;
}
</style>