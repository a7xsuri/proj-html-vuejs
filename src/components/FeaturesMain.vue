<template>
<div id="features">
    <h3 class="py-4">Key Features</h3>
    <p>Start working with <span>Landrick</span> that can provide everything you need to generate<br> awareness, drive traffic, connect.</p>
    <section>
        <div class="row">
            <div class="col-lg-3 p-4 mx-4" v-for="(item, index) in Card" :key="index">
                <span><i :class="item.icon"></i></span>
                <h5 class="fw-bold py-1">{{item.title}}</h5>
                <p>{{item.text}}</p>
                <span><a :href="item.link">Read more <i class="arrow right"></i></a></span>
            </div>
        </div>
    </section>
</div>  
</template>

<script>
import Data from "../Data.json";


export default {
    data(){
        return{
            Card: Data.CardKey
        }
    }
}
</script>

<style lang="scss">
@import "../style/vars.scss";
#features{
    margin-top: $mp-top;

    h3{
        font-weight: 600;
    }

    section{
        margin-top:80px;

        .col-lg-3{
            border: 1px solid $bordergray;
            width:20%;
            border-radius: 10px;
            box-shadow: 0px 0px 4px 3px $backgroundazure;

            a{
                text-decoration: none;

                .arrow {
                    border: solid $textblue;
                    border-width: 0 3px 3px 0;
                    display: inline-block;
                    padding: 3px;
                }

                .right {
                    transform: rotate(-45deg);
                }
            }
        }
    }
}
.square2{
    padding:20px;
    border-radius: 5px;
    background-color: $backgroundazure;
    margin-bottom:20px;
}

 span{
     color: $textblue;
     font-weight: bold;;
 }
</style>