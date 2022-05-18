<template>
  <div id="Quick">
    <p class="text-center blue">Quickstart</p>
    <h3 class="text-center font">Awesome isn't it? Let's dive in!</h3>
    <p class="text-center gray w-50">Start working with <span class="blue">Landrick</span> that can provide everything you need to generate awareness, drive traffic, connect.</p>
    
    <section class="backblue">
      <div class="row m-3 p-0 navcolor">
        <div :class="{'active': index === ActiveIndex}" class="col-lg-3"  v-for="(item, index) in Quick" :key="index" @click="changeOnClick(item, index)">{{item.QuickName}}</div>
      </div>
      <p class="textwhite" v-if="Quick[this.ActiveIndex]">{{Quick[this.ActiveIndex].Quicktext}}</p> 
    </section>
  </div>
</template>

<script>
import Data from "../Data.json";

export default {
    data(){
      return{
        Quick: Data.QuickStart,
        ActiveIndex: 0,
        index:0
      }
    },
    methods:{
      changeOnClick(item, index){
                this.ActiveIndex = index,
                console.log(this.ActiveIndex)
            },
  }
}
</script>

<style lang="scss">
@import "../style/vars.scss";

#Quick{
  margin-top: $mp-top;

  .font{
    font-weight: $font600;
    margin-bottom: 20px;
  }
}
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
  margin-top: 50px;
  height:120px;

  .row{
    padding:20px;

    .col-lg-3{
      padding: 10px 14px;
      color: white;
      text-align: center;
    }

    
  }
  
}
.textwhite{
      color: white;
      padding: 10px 15px;
    }
.active{
      background-color: $backgrounddarkblue;
      border:1px solid $backgrounddarkgray;
    }
    .navcolor{
      background-color: $backgrounddarkgray;
      border:2px solid $backgrounddarkgray;
      border-radius: 5px;
      position:relative;
      top:20px;
      width:95%;
      margin: 0 auto;
    }
</style>