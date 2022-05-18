<template>
    <div id="slider">
        <div class="col-lg-12">
            <div class="row">
                <div class="col-lg-6">
                    <div class="row">
                        <span>Development</span>
                        <h1 class="px-0">A Complete Developer Toolset</h1>
                        <p>Launch your compaign and benefit from our expertise on designing and managing coversion centered bootstrap4 html page</p>
                        <button class="start">Get Started</button>
                        <button class="doc">Documentation</button>
                        <p>Current Version: v2.6.0</p>
                    </div>
                </div>
                <div class="col-lg-6">
                    <img src="../assets/about.png" alt="">
                </div>
            </div>
        </div>
        <hr>
        <div class="photo-partners">
            <div class="row justify-content-between">
                <div class="col-lg-2 text-center" v-for="(item, index) in Photo" :key="index">
                    <img :src="require('../assets/' + item.name+'.svg')" alt="" class="loghi">
                </div>
            </div>
        </div>

    </div>
</template>

<script>
import Data from "../Data.json";

export default {
    data(){
        return{
            Photo: Data.img
        }
    }
}
</script>

<style lang="scss">
@import "../style/vars.scss";
#slider{
    background-color: $backgroundlightazure;
    padding-top:$mp-top;
    .col-lg-6{
        padding-left:20px;
    }
}

.row{
    h1{
        font-weight: bold;
    }
    span{
        width: auto;
        padding: 0px 20px;
        background-color: $backgroundazure;
        border-radius: 80px;
        color:$textblue;
        border:1px solid $bordergray;
    }
    button{
        width: auto;
        border-radius: 5px;
        padding: 10px 14px;
    }
    .start{
        color:white;
        background-color: $backgroundblue;
        border:none;
    }
    .doc{
        color: $textblue;
        border: 1px solid $borderblue;
        background-color:white;
    }
}
    .loghi{
        width: 50%;
    }
</style>