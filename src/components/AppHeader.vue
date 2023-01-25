<script>
export default {
    props:{
        navbar: Array
    }, 
    data(){
        return{
            scrolY: 0,
            fix: '',
        }
    },
    created () {
        window.addEventListener('scroll', this.handleScroll);
    },
    destroyed () {
        window.removeEventListener('scroll', this.handleScroll);
    },
    methods: {
        handleScroll (event) {
            this.scrolY = window.scrollY;
            if(this.scrolY > 800){
                this.fix = 'fixed'
            }
            else{
                this.fix = ''
            }
        }       
    }
}
</script>
<template lang="">
    <header :class="fix">
        <div class="container">
            <div class="row d-flex align-items-center">
                <div class="col-3">
                    <img src="../assets/images/logo.png" alt="">
                </div>
                <div class="col-9">
                    <div>
                        <ul class="text-end mb-0">
                            <li class="list-unstyled d-inline-block" v-for="(nav, index) in navbar"> 
                                <a class="fw-semibold text-decoration-none" href="#"><span>{{nav}}</span></a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="row">
            </div>
        </div>
    </header>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    .fixed{
        z-index: 99;
        position: fixed;
        width: 100%;
        top: 0;
        padding: 23px 0;
        transition: all 0.3s;
        background-color: rgb(38, 2, 98)
    }
    header{
        z-index: 2;
        position: absolute;
        width: 100%;
        top: 0;
        padding: 23px 0;
        ul{
            li{     
                &:last-child{
                    position: relative;
                    @include btn;
                    span {
                        color: black;
                        position: relative;
                        z-index: 6;
                        transition: all 0.3s;
                    }
                    a::before {
                        @include beforeButton;  
                        background-color: rgb(255, 223, 237);
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
                a{
                    &:hover{
                        color: $fifth;
                    }
                    transition: all 0.3s;
                    font-size: 18px;
                    color: $first;
                }
                &:not(&:last-child){
                    margin-right: 23px;
                }
            }
        }
    }
</style>