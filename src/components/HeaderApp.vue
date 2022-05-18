<template>
    <div id="header">
        <div class="row">
            <img src="../assets/logo-dark.png" class="logo">
            <ul>
                <li v-for="(item, index) in Page" :key="index"><a href="#">{{ item.title }}</a></li>
            </ul> 
        </div>
    </div>
</template>

<script>
import Data from "../Data.json";

export default {
    data(){
        return{
            Page: Data.menu,

        }
    }
}
</script>

<style lang="scss">
@import "../style/general.scss";
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