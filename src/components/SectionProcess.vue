<script>
export default {
    
}
</script>
<template lang="">
    <section>
        <div class="container">
            <div class="row pt-5">
                <div class="col-6 offset-6">
                    <div>
                        <h4 class="fw-semibold">Our Process</h4>
                        <h1 class="fw-semibold">Our Process for Your Animation Production</h1>
                        <p>We have an effective process for working on animation</p>
                    </div>
                    <div class="row text-center">
                        <div class="col-6">                            
                            <div class='card-sp'>
                                <div  class="icon mb-3">
                                    <img src="../assets/images/process1.png" alt="process1">
                                </div>
                                <div>
                                    <h2>Scripting</h2>
                                    <p>
                                        Well take your idea and create a
                                        technical script which consists
                                        of action notes and animation
                                        descriptions
                                    </p>
                                </div>
                                <div class="badge-sp d-flex align-items-end">
                                    <span class="fw-semibold">1</span> 
                                </div>
                            </div>
                        </div>
                        <div class="col-6">                            
                            <div class='card-sp'>
                                <div class="icon2 mb-3">
                                    <img src="../assets/images/process2.png" alt="process1">
                                </div>
                                <div>
                                    <h2>Pre-Production</h2>
                                    <p>
                                        Well take your idea and create a
                                        technical script which consists
                                        of action notes and animation
                                        descriptions
                                    </p>
                                </div>
                                <div class="badge-sp d-flex align-items-end">
                                    <span class="fw-semibold">2</span> 
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="image">
            <img src="../assets/images/process-thumb.png" alt="process-thumb">
        </div>
    </section>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    section{
        margin-top: 130px;
        position: relative;
        .container{
            .row{
                h4{
                    color: $third;
                }
                h1{
                    font-size: 60px;
                }
                p{
                    font-size: 18px;
                }
                .card-sp{
                    position: relative;
                    @include card;
                    border: 1px solid #f6eeff;
                    .icon{
                        background-color: #fff5f0;                    
                        border-radius: 100%;
                        width: 150px;
                        height: 150px;
                        margin: 0 auto;
                        img{
                            padding: 40px 15px;
                        }
                    }
                    .icon2{
                        background-color: #fff5f0;    
                        border-radius: 100%;
                        width: 150px;
                        height: 150px;
                        margin: 0 auto;
                        img{
                            padding: 30px 0 0 0 ;
                        }
                    }
                    .badge-sp{
                        position: absolute;
                        background-color: #f7f0ff;
                        border-radius: 0 9px 20px 20px ;
                        height: 65px;
                        top:0 ;
                        right: 30px;
                        color: #8d829c;
                        span{
                            padding: 2px 18px;
                        }
                    }
                }
            }
        }
        .image{
            position: absolute;
            top: 0;
            left: -13%;
            transition: all 0.3s;
            &:hover{
                transform: translateX(20px);
            }
        }
    }
</style>