<script>
export default {
    data(){
        return{
            membersArray: [
                {
                    img:'team1.png',
                    name:'Robert Coleman',
                    job:'Owner & Creative Director',
                },
                {
                    img:'team2.png',
                    name:'Don Woods',
                    job:'Administrator',
                },
                {
                    img:'team2.png',
                    name:'Tomas Nash',
                    job:'2d animator & Compositor',
                },
                {
                    img:'team4.png',
                    name:'Hector Vargas',
                    job:'Project Lead & Senior Animator',
                },
            ]
        }
    }
}
</script>
<template lang="">
    <section>
        <div class="container">
            <div class="row text-center m-sp">
                <div class="col-12">
                    <h4 class="fw-semibold">Anidio Magic Team Member</h4>
                    <h1 class="fw-semibold">Let Us Animate Your <br> Project</h1>
                    <p>We create new worlds!Let's collaborate and create engaging, effective, <br> award-winning animations</p>
                </div>
            </div>
            <div class="row">
                <div class="col-3 text-center" v-for="(mem, index) in  membersArray" :key="index">
                    <div class="bg-sp">
                        <div class="member">
                            <img :src="`src/assets/images/${mem.img}`" alt="mem">
                        </div>
                        <div class="info-sp">
                            <h3 class="fw-semibold mb-3">{{mem.name}}</h3>
                            <h6>{{mem.job}}</h6>
                        </div>
                        <div class="social">
                            <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                            <a href="#"><i class="fa-brands fa-twitter"></i></a>
                            <a href="#"><i class="fa-brands fa-instagram"></i></a>
                        </div>
                    </div>
                </div>
            </div>
            <div class="row text-center mt-5">
                <div class="col-12 d-flex align-items-center justify-content-center">
                    <div class="btn-sp">
                        <button><i class="fa-solid fa-arrow-left"></i></button>
                    </div>
                    <div class="btn-point">
                        <button></button>
                        <button></button>
                        <button></button>
                    </div>
                    <div class="btn-sp">
                        <button><i class="fa-solid fa-arrow-right"></i></button>
                    </div>
                </div>
            </div>
        </div>
        <div class="shape">
            <img src="../assets/images/shape.png" alt="shape">
        </div>
        <div class="shape2">
            <img src="../assets/images/shape2.png" alt="shape">
        </div>
    </section>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    section{
        position: relative;
        overflow: hidden;
        .container{
            .m-sp{
                margin-bottom: 180px;
            }
            .row{
                h4{
                    color: $third;
                }
                h1{
                    font-size: 60px;
                    color: $second;
                }
                p{
                    font-size: 18px;
                    color: $second;
                }
                .btn-point{
                    button{
                        margin: 8px;
                        height: 10px;
                        width: 10px;
                        background-color: $eighth;
                        border-radius: 100% ;
                    }
                }
                .btn-sp{
                    @include btn-arrow;
                    border: 1px solid $eighth;
                    transition: all 0.3s;
                    &:hover{
                        background-color: $fifth;
                        color: $first
                    }
                }
                .bg-sp{
                    background-color: #fff5f0;
                    border-radius: 20px;
                    padding-bottom: 40px ;
                    .member{
                        margin: -60px 0;
                        transform: translateY(-80px);
                        transition: all 0.3s;
                    }
                    .info-sp{
                        margin-bottom: 30px;
                    }
                    .social{
                        a{
                            transition: all 0.3s;
                            &:hover{
                                background-color: $fifth;
                                color: $first
                            }
                            background-color: $first;
                            color: $third;
                            padding: 12px 15px;
                            border: 1px solid $eighth;
                            border-radius: 100% ;
                            &:not(&:last-child){
                                margin-right: 15px;
                            }
                            &:first-child{
                                padding: 12px 18px;
                            }
                        }
                    }
                }
            }
        }
        .shape{
            position: absolute;
            top:0;
            left: 0;
            animation: scaleX 4s linear infinite;
            animation-direction: alternate;
            @keyframes scaleX {
                0%{
                    transform: scale(1);
                }
                100%{
                    transform: scale(0.9);
                }
            }
        }
        .shape2{
            position: absolute;
            top:0;
            right: 0;
            animation: shakeX 4s linear infinite;
            max-width: 680px;
            animation-direction: alternate;
            @keyframes shakeX {
                100%{
                    transform: translateX(50px);
                }
            }
        }
    }
</style>