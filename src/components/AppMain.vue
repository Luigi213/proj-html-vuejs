<script>
export default {

}
</script>
<template lang="">
    <main>
        <section class="jumbo">
            <div class="container">
                <div class="row text-center">
                    <div class="col-12">
                        <h4 class="fw-semibold">Imagine, Create, Experience</h4>
                        <h1 class="fw-semibold">We Animate <br> With Ninja-Like Precision</h1>
                        <p class="fs-5">We are a character-driven animation studio striving to make high-quality animations.</p>
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
            <div class="wave"></div>
        </section>
    </main>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    main{
        .jumbo{
            position: relative;
            padding: 170px 0 0;
            margin-bottom: 200px;
            background: url('../assets/images/banner-bg.png') no-repeat center;
            background-size: cover;
            .container{
                h4{
                    color: $fifth;
                }
                h1{
                    font-size: 70px ;
                    color: $first
                }
                p{
                    color: $first
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
            .wave{
                width: 100%;
                height: 100%;
                position: absolute;
                bottom:0;
                background: url('../assets/images/bottom-shape.png') no-repeat bottom;
            }
        }
    }
</style>