<script>
export default {
    data(){
        return{
            workArray:[
                {
                    img:'work1.png',
                },
                {
                    img:'work2.png',
                },
                {
                    img:'work3.png',
                },
                {
                    img:'work4.png',
                },
            ]
        }
    }
}
</script>
<template lang="">
    <section>
        <div class="container">
            <div class="row justify-content-center text-center">
                <div class="col-12">
                    <h5 class="fw-semibold">Our Works</h5>
                    <h1 class="fw-semibold">Featured Productions</h1>
                    <p>Here's just a small sample of some of those projects that we're quite proud of. <br> If you're looking for something specific feel free to get in contact with us.</p>
                </div>
            </div>
            <div class="row gy-4 mt-3">
                <div class="col-6" v-for="(work, index) in workArray" :key="index">
                    <img :src="`src/assets/images/${work.img}`" :alt="`work${index}`">
                    <div class="overlay">
                        <a class="d-flex justify-content-center align-items-center text-decoration-none" href="#"><i class="fa-solid fa-play fs-2"></i></a>
                    </div>
                </div>
                <div class="col-12 text-center mt-5">
                    <div class="btn">
                        <a class="fw-semibold text-decoration-none" href="#"><span>See Our Work</span></a>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    section{
        margin-top: 130px ;
        .container{
            .row{
                .col-12{
                    h5{
                        font-size: 25px;
                        color: $third
                    }
                    h1{
                        font-size: 62px;
                    }
                    .btn{
                        @include btn;
                        border: 1px solid $fourth;
                    }
                }
                p{
                    font-size: 18px;
                }
                .col-6{
                    transition: all 0.3s;
                    position: relative;
                    z-index: 0;
                    &:hover{
                        transform: skewX(5deg);
                        .overlay{
                            opacity: 1;
                            visibility: visible;
                            transform: scale(1);
                        }
                    }
                    .overlay{
                        width: 96%;
                        height: 100%;
                        position:absolute;
                        top: 0;
                        z-index: 2;
                        background: rgba(56, 53, 196, 0.25);
                        border-radius: 20px;
                        transform: scale(0);
                        visibility: hidden;
                        opacity: 0.8;
                        transition: all 0.6s;
                        a{
                            height: 100%;
                            i{
                                @include btn-sp;
                                background-color: $first;
                                color: $fifth;
                            }
                        }
                    }
                }
                .btn{
                    position: relative;
                    @include btn;
                    margin: 15px ;
                    span {
                        color: black;
                        position: relative;
                        z-index: 6;
                        transition: all 0.3s;
                    }
                    a::before {
                        @include beforeButton;  
                    }
                    a::after {
                        @include afterButton;
                    }
                    a:hover::before{
                        opacity: 0;
                        transform: scale(0.5, 0.5);
                    }
                    a:hover::after {
                        opacity: 1;
                        transform: scale(1, 1);
                    }    
                }        
            }
        }
    }
</style>