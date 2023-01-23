<script>
export default {
    
}
</script>
<template lang="">
    <section class="jumbo">
        <div class="container">
            <div class="row text-center">
                <div class="col-12">
                    <h4 class="fw-semibold">Imagine, Create, Experience</h4>
                    <h1 class="fw-semibold">We Animate <br> With Ninja-Like Precision</h1>
                    <p class="font-sp">We are a character-driven animation studio striving to make high-quality animations.</p>
                </div>
                <div class="col-12 my-3">
                    <div class="btn">
                        <button>Start Project</button>
                    </div>
                    <div class="btn">
                        <button>Portfolio</button>
                    </div>
                </div>
                <div class="col-12 mt-5 ">
                    <div class="image">
                        <img src="../assets/images/middle.png" alt="">
                    </div>
                </div>
            </div>
        </div>
        <div class="dots d-flex">
            <div class="dots-left">
                <img src="../assets/images/dots-left.png" alt="dots-left">
            </div>
            <div class="dots-right">
                <img src="../assets/images/dots-right.png" alt="dots-right">
            </div>
        </div>
        <div class="mans d-flex justify-content-between w-100">
            <div class="man-left">
                <img src="../assets/images/left-man.png" alt="man-left">
            </div>
            <div class="man-right">
                <img src="../assets/images/right-man.png" alt="man-right">
            </div>
        </div>
        <div class="globe1">
            <img src="../assets/images/globe1.png" alt="globe1">
        </div>
        <div class="globe2">
            <img src="../assets/images/globe2.png" alt="globe2">
        </div>
        <div class="globe3">
            <img src="../assets/images/globe3.png" alt="globe3">
        </div>
        <div class="light">
            <img src="../assets/images/light.png" alt="light">
        </div>
        <div class="wave">
            <img src="../assets/images/bottom-shape.png" alt="wave">
        </div>
    </section>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    .jumbo{
        position: relative;
        padding: 170px 0 0;
        margin-bottom: 200px;
        background: url('../assets/images/banner-bg.png') no-repeat center;
        background-size: cover;
        .container{
            .row{
                .col-12{
                    h4{
                        color: $fifth;
                    }
                    h1{
                        font-size: 80px ;
                        color: $first
                    }
                    p{
                        color: $first
                    }
                    .font-sp{
                        font-size: 23px;
                    }
                    .btn{
                        &:first-child{
                            button{
                                @include btn;
                                background-color: $first;
                            }
                        }
                        &:last-child{
                            button{
                                @include btn;
                                border: 1px solid $first;
                                color: $first;
                            }
                        }
                    }
                    .image{
                        img{
                            margin-top: -200px ;
                            transform: translateY(200px);
                            z-index: 99;
                            position: relative;
                        }
                    }
                }
            }
        }
        .dots{
            top: 0;
            .dots-left, .dots-right{
                width: 50%;
                img{
                    width: 100%;
                }
            }
        }
        .mans{
            z-index: 2;
            top: 27%;
            animation: fly 3s linear infinite;
            @keyframes fly {
                0%{
                    transform: translateY(0px);
                }
                50%{
                    transform: translateY(-15px);
                }
                100%{
                    transform: translateY(0px);
                }
            }
        }
        .globe1{
            top:11%;
            left: 9%;
            width: 126px;
            animation: glob1 4s linear infinite ;
            @keyframes glob1 {
                0%{
                    transform: rotate(360deg);
                }
            }
        }
        .globe2{
            width: 100px;
            top: 17%;
            right: 28%;
            animation: glob2 4s linear infinite ;
            @keyframes glob2 {
                0%{
                    transform: rotate(360deg);
                }
            }
        }
        .globe3{
            width: 300px;
            top: -20%;
            left: 33%;
        }
        .light{
            top:10%;
            right: 9%;
            animation: ligh 3s linear infinite;
            @keyframes ligh {
                50%{
                    transform: rotate(10deg);
                } 
                100%{
                    transform: rotate(0deg);
                }
            }
        }
        .wave{
            width: 100%;
            height: 163px;
            bottom: -1px;
            left: 0;
            img{
                height: 100%;
            }
        }
        .globe1, .globe2, .globe3, .light, .mans, .dots, .wave{
            position: absolute;
        } 
    }
</style>