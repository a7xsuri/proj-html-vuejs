<template>
    <div id="rates">
        <h3 class="text-center">Our rates for developer from landrick team</h3>
        <p class="text-center my-3">Star working with <span>Landrick</span> that can provide everything you need to generate<br> awareness, drive traffic, connect.</p>
        <div class="row mt-5">
            <div class="col-lg-4 p-3 mx-3" v-for="(item, index) in Card" :key="index">
                <span class="type">{{item.plan}}</span>
                <h3 class="fw-bold mt-3">{{item.cost}}</h3>
                <p>Per Month</p>
                <p class="w-75">{{item.Caratteristic}}</p>
                <hr>
                <ul class="ps-0">
                    <li v-for="(number, index) in item.Tools" :key="index"><i class="fa-regular fa-circle-check check"></i> {{number}}</li>
                </ul>
                <button class="buy">Buy Now</button>
                <p class="my-3">*No credit card required</p>
            </div>
        </div>
    </div>
</template>
<script>
import Data from "../Data.json";

export default {
    data(){
        return{
            Card: Data.RatesCard
        }
    }
}
</script>

<style lang="scss">
@import "../style/vars.scss";
#rates{
    margin-top: $mp-top;

    h3{
        font-weight: $font600;
    }

    .col-lg-4{
        border-radius: 10px;
        border:1px solid $bordergray;
        width: 30%;
        box-shadow: 0px 7px 1px -4px #00000063;

        .type{
            background-color: $backgroundazure;
            padding: 5px 10px;
            border-radius: 20px;
        }

        .buy{
            color: white;
            background-color: $backgroundblue;
            border: none;
            width: 100%;
        }

        ul{
            list-style-type: none;
        }
    }
}
</style>