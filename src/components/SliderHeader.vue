<template>
    <div id="slider">
        <div class="col-lg-12">
            <div class="row">
                <div class="col-lg-6 padd">
                    <div class="row">
                        <span class="oval">Development</span>
                        <h1 class="px-0">A Complete<br> Developer Toolset</h1>
                        <p class="px-0 py-2">Launch your compaign and benefit from our expertise on designing<br> and managing coversion centered bootstrap4 html page</p>
                        <button class="start">Get Started</button>
                        <button class="doc">Documentation</button>
                        <p class="px-0 py-2">Current Version: v2.6.0</p>
                    </div>
                </div>
                <div class="col-lg-6">
                    <img src="../assets/about.png" alt="">
                </div>
            </div>
        </div>
        <hr class="mw">
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
    .padd{
        padding-top:80px;
    }
}
.mw{
    width: 119%;
    margin-left: -126px;
    margin-top: $mp-top;
}
.row{
    h1{
        font-weight: bold;
        line-height: 1.5;
    }
    .oval{
        width: auto;
        padding: 0px 20px;
        background-color: $backgroundazure;
        border-radius: 80px;
        color:$textblue;
        box-shadow: 0px 0px 3px 1px $backgroundazure;
        margin-bottom:10px;
    }
    button{
        width: auto;
        border-radius: 5px;
        padding: 7px 14px;
        font-weight: bold;
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
        margin-left: 10px;
    }
}
    .loghi{
        width: 50%;
    }
</style>