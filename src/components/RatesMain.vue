<template>
    <div id="rates">
        <h3>Our rates for developer from landrick team</h3>
        <p>Star working with Landrick that can provide everything you need to generate awareness, drive traffic, connect.</p>
        <div class="row">
            <div class="col-lg-4 p-3" v-for="(item, index) in Card" :key="index">
                <span class="type">{{item.plan}}</span>
                <h3>{{item.cost}}</h3>
                <p>Per Month</p>
                <p>{{item.Caratteristic}}</p>
                <hr>
                <ul>
                    <li v-for="(number, index) in item.Tools" :key="index">{{number}}</li>
                </ul>
                <button class="buy">Buy Now</button>
                <p>*No credit card required</p>
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

    .col-lg-4{
        border-radius: 10px;
        border:1px solid $bordergray;

        .buy{
            color: white;
            background-color: $backgroundblue;
            border: none;
            width: 100%;
        }
    }
}
</style>