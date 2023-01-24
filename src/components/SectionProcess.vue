<script>
export default {
    data(){
        return{
            width: -646,
            active: 0,
            autoplay: null,
            processArray: [
                {
                    id: 3,
                    img: 'process1.png',
                    title: 'Scripting',
                    pagraph: 'Well take your idea and create a technical script which consists of action notes and animation descriptions',
                },
                {
                    id: 4,
                    img: 'process2.png',
                    title: 'Pre-Production',
                    pagraph: 'Well take your idea and create a technical script which consists of action notes and animation descriptions'
                },
                {
                    id: 1,
                    img: 'process1.png',
                    title: 'Scripting',
                    pagraph: 'Well take your idea and create a technical script which consists of action notes and animation descriptions'
                },
                {
                    id: 2,
                    img: 'process2.png',
                    title: 'Pre-Production',
                    pagraph: 'Well take your idea and create a technical script which consists of action notes and animation descriptions'
                },
                {
                    id: 3,
                    img: 'process1.png',
                    title: 'Scripting',
                    pagraph: 'Well take your idea and create a technical script which consists of action notes and animation descriptions',
                },
                {
                    id: 4,
                    img: 'process2.png',
                    title: 'Pre-Production',
                    pagraph: 'Well take your idea and create a technical script which consists of action notes and animation descriptions'
                },
                {
                    id: 1,
                    img: 'process1.png',
                    title: 'Scripting',
                    pagraph: 'Well take your idea and create a technical script which consists of action notes and animation descriptions'
                },
            ]
        }
    },
    mounted(){
        this.automatic()
    },
    methods:{
        next(){
            this.width += -313
            if(this.width < -1615){
                this.width = -646
            }
        },      
        prev(){
            this.width += +313
            if(this.width > -646){
                this.width = -1615
            }
        },
        automatic(){
            this.autoplay = setInterval(() => {
                this.next()
            }, 2000);
        }
    }
}
</script>
<template lang="">
    <section>
        <div class="container">
            <div class="row pt-5 overflow">
                <div class="col-6 offset-6">
                    <div>
                        <h4 class="fw-semibold">Our Process</h4>
                        <h1 class="fw-semibold">Our Process for Your Animation Production</h1>
                        <p>We have an effective process for working on animation</p>
                    </div>
                    <div class="w-sp">
                        <div class="d-flex text-center" :style="{transform:`translate3d(${width}px, 0px, 0px)`, transition: 'all 0.6s ease 0s', width: '2584px'}">
                            <div :style="{width:'313px', margin: '0 10px 0 0'}" :class="(active === index) ? 'active' : ''" v-for="(process, index) in processArray" :key="index">
                                <div class='card-sp'>
                                    <div  class="icon mb-3"> 
                                        <img :src="`src/assets/images/${process.img}`" alt="process1">
                                    </div>
                                    <div>
                                        <h2>{{process.title}}</h2>
                                        <p>
                                            {{process.pagraph}}
                                        </p>
                                    </div>
                                    <div class="badge-sp d-flex align-items-end">
                                        <span class="fw-semibold">{{process.id}}</span> 
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                        <!-- <div class="col-6 hidden" :class="(active + 1 === index) ? 'visibility' : ''" v-for="(process, index) in processArray" :key="index">
                            <div class='card-sp'>
                                <div  class="icon mb-3"> 
                                    <img :src="`src/assets/images/${process.img}`" alt="process1">
                                </div>
                                <div>
                                    <h2>{{process.title}}</h2>
                                    <p>
                                        {{process.pagraph}}
                                    </p>
                                </div>
                                <div class="badge-sp d-flex align-items-end">
                                    <span class="fw-semibold">{{process.id}}</span> 
                                </div>
                            </div>
                        </div> -->
                </div>
            </div>
            <div class="row mt-3">
                <div class="col-6 offset-6">
                    <div class="btn-sp">
                        <button @click="prev"><i class="fa-solid fa-arrow-left"></i></button>
                        <button @click="next"><i class="fa-solid fa-arrow-right"></i></button>
                    </div>
                </div>
            </div>
        </div>
        <div class="image">
            <img src="../assets/images/process-thumb.png" alt="process-thumb">
        </div>
        <div class="smart4">
            <img src="../assets/images/smart4.png" alt="smart4">
        </div>
    </section>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    section{
        margin-top: 130px;
        padding-bottom: 185px ;
        position: relative;
        .container{
            .overflow{
                overflow: hidden;
            }
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
                .w-sp{
                    width: 100%;
                    overflow: hidden;
                    .col{

                    }
                }
                .hidden{
                    display: none;
                }
                .hidden.visibility{
                    transition: all 0.3s;
                    animation: d-play 3s;
                    @keyframes d-play {
                        from{
                            transform: translateX(-200px);
                            opacity: 0;
                        }
                        to{
                            transform: translateX(50px);
                            opacity: 1;
                        }
                    }
                    display: block;
                }
                .btn-sp{
                    button{
                        transition: all 0.3s;
                        &:hover{
                            background-color: $fifth;
                            color: $first
                        }
                        color: $third;
                        border: 1px solid $sixth;
                        @include btn-arrow;
                        margin-right: 15px ;
                    }
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