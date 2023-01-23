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
            position: absolute;
            top: 0;
            .dots-left, .dots-right{
                width: 50%;
                img{
                    width: 100%;
                }
            }
        }
        .mans{
            position: absolute;
            z-index: 2;
            top: 26%;

        }
        .wave{
            width: 100%;
            height: 160px;
            position: absolute;
            bottom:0;
            left: 0;
            img{
                width: 100%;
                height: 100%;
            }
        }
    }
</style>