<template>
  <div id="main">
    <features-main/>
    <quick-main/>
    <tools-main/>
    <rates-main/>
    <among-main/>
  </div>
</template>

<script>
import FeaturesMain from './FeaturesMain.vue';
import QuickMain from './QuickMain.vue';
import ToolsMain from './ToolsMain.vue';
import RatesMain from './RatesMain.vue';
import AmongMain from './AmongMain.vue';


export default {
  components: {
      FeaturesMain,
      QuickMain,
      ToolsMain,
      RatesMain,
      AmongMain
      },

}
</script>

    
<style lang="scss">
</style>