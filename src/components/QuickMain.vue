<template>
  <div id="Quick">
    <p class="text-center blue">Quickstart</p>
    <h3 class="text-center">Awesome isn't it? Let's dive in!</h3>
    <p class="text-center gray w-50">Start working with <span class="blue">Landrick</span> that can provide everything you need to generate awareness, drive traffic, connect.</p>
    
    <section class="backblue">
      <div class="row mx-0">
        <div class="col-lg-3" v-for="(item, index) in Quick" :key="index">{{item.QuickName}}</div>
        <!-- <p v-if="item.Active==true">{{item.text}}</p> -->
      </div>
    </section>
  </div>
</template>

<script>
import Data from "../Data.json";

export default {
    data(){
        return{
          Quick: Data.QuickStart
        }
    }
}
</script>

<style lang="scss">
@import "../style/vars.scss";
.blue{
  color: $textblue;
  font-weight: 600;
}

.gray{
  color: $backgrounddarkgray;
  margin: 0 auto;
}
.backblue{
  width: 50%;
  border-radius:10px;
  margin: 0 auto;
  background-color: $backgrounddarkblue;

  .row{
    padding:20px;
    
    .col-lg-3{
      padding: 10px 14px;
      color: white;
      text-align: center;
      background-color: $backgrounddarkgray;
    }
  }
  
}
</style>