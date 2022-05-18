<template>
    <div id="header">
        <div class="container">
            <div class="row">
                <img src="../assets/logo-dark.png" class="logo">
                <ul>
                    <li v-for="(item, index) in Page" :key="index"><a href="#">{{ item.title }}</a></li>
                </ul>
                <ul>
                    <li><font-awesome-icon icon="fa-solid fa-magnifying-glass" /></li>
                    <li><font-awesome-icon icon="fa-brands fa-github" /></li>
                    <li><font-awesome-icon icon="fa-solid fa-book-open" /></li>
                    <li><font-awesome-icon icon="fa-light fa-user" /></li>
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
        justify-content: space-between;
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
            }
        }
    }
}


</style>