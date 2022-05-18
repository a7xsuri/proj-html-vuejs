<template>
<div id="features">
    <h3>Key Features</h3>
    <p>Start working with <span>Landrick</span> that can provide everything you need to generate awareness, drive traffic, connect.</p>
    <section>
        <div class="row">
            <div class="col-lg-3" v-for="(item, index) in Card" :key="index">
                <h5>{{item.title}}</h5>
                <p>{{item.text}}</p>
                <span><a :href="item.link">Read more</a></span>
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
 span{
     color: $textblue;
     font-weight: bold;;
 }
</style>