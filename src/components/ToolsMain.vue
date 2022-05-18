<template>
    <div id="tools">
        <div class="col-lg-12">
            <div class="row">
                <div class="col-lg-6 py-5">
                    <h3 class="font mb-4">Build tools and<br> extensive documention</h3>
                    <p class="gray my-3">you can combine all the Landrick templates into a single one, you can take a component from the Application theme and use it in the Website.</p>
                    <ul class="px-0">
                        <li class="gray lh"><i class="fa-regular fa-circle-check check"></i> Digital Marketing Solutions fot Tomorrow</li>
                        <li class="gray lh"><i class="fa-regular fa-circle-check check"></i> Our Talented & Experienced MArketing Agency</li>
                        <li class="gray lh"><i class="fa-regular fa-circle-check check"></i> Create your own skun to match your brand</li>
                    </ul>
                    <button class="purple">Read More</button>
                </div>
                <div class="col-lg-6">
                    <img src="../assets/1.png" alt="" class="w-75 mleft">
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
    line-height: 1.5;
}

.mleft{
    margin-left:35px;
}
.gray{
    color: $backgrounddarkgray;
}

.lh{
 line-height: 2;
}

ul{
    list-style-type: none;
}

.check{
    color: $violet;
    font-size:17px;
}

.purple{
    border:none;
    border-radius: 10px;
    color: white;
    background-color: $violet;
}
</style>