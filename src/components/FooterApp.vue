<template>
    <div id="footer">
        <div class="container">
            <div class="row py-5 white">
                <div class="col-lg-3">
                    <img src="../assets/logo-light.png" alt="" class="logo-footer pb-4">
                    <p class="">Start working with Landrick that can provide everything you need to generate awareness, drive traffic, connect.</p>
                    <div class="social">
                        <i class="fa-regular fa-user bord mx-1"></i>
                        <i class="fa-regular fa-user bord mx-1"></i>
                        <i class="fa-regular fa-user bord mx-1"></i>
                        <i class="fa-regular fa-user bord mx-1"></i>
                    </div>
                </div>
                <div class="col-lg-3" v-for="(element, index) in Mfooter" :key="index">
                    <h3>{{element.title}}</h3>
                    <ul class="px-0">
                        <li v-for="(page, index) in element.SubPages" :key="index"><i class="arrow right"></i><a href="#"> {{page}}</a></li>
                    </ul>
                </div>
                <div class="col-lg-3">
                    <h3 class="fw-bold">Newsletter</h3>
                    <p>Sign up and receive the latest tips<br> via email.</p>
                    <div class="mb-3">
                        <label for="exampleFormControlInput1" class="form-label">Write your Email<span class="red">*</span></label>
                        <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="Your Email:">
                        <button class="mt-4 subs">Subscribe</button>
                    </div>
                </div>
            </div>
            <hr class="mw">
            <div class="row justify-content-between">
                <div class="credits w-50">
                    <p class="white"><i class="fa-regular fa-copyright"></i> 2020 Landrick. Design with <i class="fa-solid fa-heart red"></i> by Shreethemes</p>
                </div>
                <div class="payaments w-50">
                    <img src="../assets/american-ex.png" alt="">
                    <img src="../assets/discover.png" alt="">
                    <img src="../assets/master-card.png" alt="">
                    <img src="../assets/paypal.png" alt="">
                    <img src="../assets/visa.png" alt="">
                </div>
            </div>
        </div>
        
    </div>
</template>

<script>
import Data from "../Data.json"
export default {
    data(){
        return{
            Mfooter: Data.menufooter
        }
    }
}
</script>

<style lang="scss">
@import "../style/vars.scss";
#footer{
    margin-top: $mp-top;
    padding-bottom: 20px;

    ul{
        list-style-type: none;
        a{
            text-decoration: none;
            color:white;
        }
        .arrow {
                    border: solid white;
                    border-width: 0 3px 3px 0;
                    display: inline-block;
                    padding: 3px;
                }

                .right {
                    transform: rotate(-45deg);
                }
    }
}
.logo-footer{
    width: 50%;
}
.subs{
    color: $textblue;
    background-color: $backgrounddarkblue;
    box-shadow: 0px 2px 7px 1px $textblue;
    border:none;
    border-radius:7px;
    width: 100%;
}
.white{
    color: white;

    .bord{
        padding: 7px;
        border: 2px solid white;
        border-radius:5px;
    }
}
.red{
        color: red;
    }
.credits{

    i{
        font-size:14px;
    }
    
}
.payaments{

    text-align: end;
    img{
        width:6%;
        margin-left: 1px;
    }
}
</style>