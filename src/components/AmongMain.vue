<template>
    <div id="among" class="text-center">
        <h3>Want to be among the first to find out?</h3>
        <p class="my-3">Star working with <span class="blue">Landrick</span> that can provide everything you need to generate<br> awareness, drive traffic, connect.</p>
        <div class="input-group mb-3 wd">
            <input type="text" class="form-control br w-50" placeholder="Recipient's username" aria-label="Recipient's username" aria-describedby="basic-addon2">
            <span class="input-group-text start" id="basic-addon2"> Get Started</span>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import "../style/vars.scss";
#among{
    margin-top: $mp-top;

    h3{
        font-weight: $font600;
    }

    .wd{
        margin: 0 auto;
        width:50%
    }

    .blue{
        color:$textblue;
        font-weight: bold;
    }

    .br{
        border-radius: 25px;
    }

    .start{
        color:white;
        background-color: $backgroundblue;
        border:none;
        border-radius: 41px;
        margin-left: -106px;
        z-index: 1;
        padding: 0px 12px;
        height: 33px;
        margin-top: 2px;
    }
}
</style>