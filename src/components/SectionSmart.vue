<script>
export default {
    
}
</script>
<template lang="">
    <section class="Animetion">
        <div class="container">
            <div class="row">
                <div class="col-9 offset-3 text-center">
                    <div class="row">
                        <div class="col-10 fade">
                            <h5 class="fw-semibold fs-4">Our Love For Animation</h5>
                            <h1 class="fw-semibold">We're Storytelling Experts With Creative Smarts</h1>
                            <p>Our culture inspires the creative and innovative spirit found throughout our Studio. We breathe life into new ideas!</p>                                
                        </div>                                            
                    </div>
                    <div class="row mt-5">
                        <div class="col-4">
                            <div class="card-sp-sm1 text-center">
                                <img src="../assets/images/smart1.png" alt="smart1">
                                <h3 class="mt-3 fw-semibold">3D modeling</h3>
                                <p>We constantly ask questions. It helps us shape your story and deliver the results you crave. Yep, we'll drill deep to deliver above and beyond your expectations.</p>                      
                            </div>
                        </div>
                        <div class="col-4">
                            <div class="card-sp-sm2 text-center"> 
                                <img src="../assets/images/smart2.png" alt="smart2">
                                <h3 class="mt-3 fw-semibold">Collaboration</h3>         
                                <p>We constantly ask questions. It helps us shape your story and deliver the results you crave. Yep, we'll drill deep to deliver above and beyond your expectations.</p>                       
                            </div>
                        </div>
                        <div class="col-4">
                            <div class="card-sp-sm3 text-center">              
                                <img src="../assets/images/smart3.png" alt="smart3">                  
                                <h3 class="mt-3 fw-semibold">Creativity</h3>
                                <p>We constantly ask questions. It helps us shape your story and deliver the results you crave. Yep, we'll drill deep to deliver above and beyond your expectations.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="smart">
            <img src="../assets/images/smart.png" alt="smart">
        </div>
        <div class="smart4">
            <img src="../assets/images/smart4.png" alt="smart4">
        </div>
    </section>
</template>
<style lang="scss" scoped> 
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    .Animetion{
        padding: 130px 0;
        position: relative;        
        .smart{            
            width: 500px;
            height: 900px;
            position: absolute;
            top:0;
            left: 0;
            img{
                width: 100%;
                height: 100%;
            }
        }
        .smart4{
            width: 145px;
            height: 145px;
            position: absolute;
            bottom: 0;
            right: 0;
            object-fit: cover;
            img{
                width: 100%;
                height: 100%;
            }
        }
        .container{
            .row{
                .fade{
                    opacity: 1;
                    animation: fadeDown 2s linear;
                    @keyframes fadeDown {
                        0%{
                            opacity: 0;
                            transform: translateY(-20px);
                        }
                        100%{
                            opacity: 1;
                            transform: translateY(0);
                        }
                    }
                }
                .col-10{
                    h5{
                        color: $third;
                    }
                    h1{
                        font-size: 60px;
                    }
                    p{
                        width: 77%;
                        font-size: 18px ;
                        margin: 0 auto;
                    }
                }
                .card-sp-sm1{
                    background-image: -webkit-linear-gradient(90deg, rgba(255, 122, 31, 0.10196) 0%, rgba(1, 5, 48, 0) 100%);
                    &:hover{
                        background-image: -webkit-linear-gradient(270deg, rgba(255, 122, 31, 0.10196) 0%, rgba(1, 5, 48, 0) 100%);
                        outline: 1px solid $first;
                    }
                }
                .card-sp-sm2{
                    background-image: -webkit-linear-gradient(90deg, rgba(77, 54, 220, 0.10196) 0%, rgba(1, 5, 48, 0) 100%);
                    &:hover{
                        background-image: -webkit-linear-gradient(270deg, rgba(77, 54, 220, 0.10196) 0%, rgba(1, 5, 48, 0) 100%);
                        outline: 1px solid $first;
                    }
                }
                .card-sp-sm3{
                    background-image: -webkit-linear-gradient(90deg, rgba(255, 0, 15, 0.10196) 0%, rgba(1, 5, 48, 0) 100%);
                    &:hover{
                        background-image: -webkit-linear-gradient(90deg, rgba(255, 0, 15, 0.10196) 0%, rgba(1, 5, 48, 0) 100%);
                        outline: 1px solid $first;
                    }
                }
                .card-sp-sm1, .card-sp-sm2, .card-sp-sm3{
                    position: relative;
                    z-index: 1;
                    @include card;
                    transition: all 0.4s;
                    outline: 1px solid rgb(213, 213, 213);
                    p{
                        font-size: 18px
                    }
                }
            }
        }
    }
</style>