<template>
    <div id="header">
        <div class="container">
            <div class="row justify-content-between">
                <img src="../assets/logo-dark.png" class="logo">
                <ul>
                    <li v-for="(item, index) in Page" :key="index"><a href="#">{{ item.title }}</a><i v-if="item.toggle" class="arrow down"></i></li>
                </ul>
                <ul>
                    <li class="px-1"><i class="fa-solid fa-magnifying-glass"></i></li>
                    <li class="px-1"><i class="fa-solid fa-code-branch square"></i></li>
                    <li class="px-1"><i class="fa-solid fa-book square"></i></li>
                    <li class="px-1"><i class="fa-regular fa-user square"></i></li>
                </ul>
            </div>
            <slider-header/>
        </div>
    </div>
</template>

<script>
import Data from "../Data.json";
import SliderHeader from './SliderHeader.vue';

export default {
    components:{
        SliderHeader
    },
    data(){
        return{
            Page: Data.menu,
        }
    }
}
</script>

<style lang="scss">
@import "../style/vars.scss";
#header{
    padding: 20px;
    background-color: $backgroundlightazure;

    .row{
        
        .logo {
            width: $widthlogo;
            height: $widthlogo;
        }

        ul{
            list-style-type: none;
            width: auto;

            li{
                float:left;
                padding:0px 20px;

                a{
                    text-decoration: none;
                    color: $textblack;
                }

                .arrow {
                    border: solid black;
                    border-width: 0 3px 3px 0;
                    display: inline-block;
                    padding: 3px;
                    margin-left: 5px;
                    margin-bottom: 3px;
                
                }
                .down {
                    transform: rotate(45deg);
                    -webkit-transform: rotate(45deg);
                }
            }
        }
    }
}
i{
    font-size:22px;
}
.square{
    padding:10px;
    border-radius: 10px;
    border: none;
    background-color: $backgroundazure;
    margin-top:-9px;
	box-shadow: 0 7px 9px -6px $backgroundblue;
    color: $textblue;
}

</style>