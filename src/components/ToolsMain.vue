<template>
    <div id="tools">
        <div class="col-lg-12">
            <div class="row">
                <div class="col-lg-6 py-2">
                    <h3 class="font">Build tools and<br> extensive documention</h3>
                    <p class="gray">you can combine all the Landrick templates into a single one, you can take a component from the Application theme and use it in the Website.</p>
                    <ul>
                        <li class="gray">Digital Marketing Solutions fot Tomorrow</li>
                        <li class="gray">Our Talented & Experienced MArketing Agency</li>
                        <li class="gray">Create your own skun to match your brand</li>
                    </ul>
                    <button class="purple">Read More</button>
                </div>
                <div class="col-lg-6">
                    <img src="../assets/1.png" alt="" class="w-75">
                </div>
            </div>
        </div> 
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import "../style/vars.scss";
#tools{
    margin-top: $mp-top;
}

.font{
    font-weight: $font600;
}

.gray{
    color: $backgrounddarkgray;
}

.purple{
    border:none;
    border-radius: 10px;
    color: white;
    background-color: $violet;
}
</style>