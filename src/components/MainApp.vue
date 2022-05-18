<template>
  <div id="main">
    <slider-main/>
    <features-main/>
    <quick-main/>
    <tools-main/>
    <rates-main/>
    <landrick-main/>
  </div>
</template>

<script>
import FeaturesMain from './FeaturesMain.vue';
import SliderMain from './SliderMain.vue';
import QuickMain from './QuickMain.vue';
import ToolsMain from './ToolsMain.vue';
import RatesMain from './RatesMain.vue';
import LandrickMain from './RatesMain.vue';


export default {
  components: { 
      SliderMain,
      FeaturesMain,
      QuickMain,
      ToolsMain,
      RatesMain,
      LandrickMain
      },

}
</script>

    
<style lang="scss">
</style>