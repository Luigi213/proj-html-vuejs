<script>
export default {
    props:{
        navbar: Array
    },
}
</script>
<template lang="">
    <header class="down-scroll">
        <div class="container">
            <div class="row d-flex align-items-center">
                <div class="col-3">
                    <img src="../assets/images/logo.png" alt="">
                </div>
                <div class="col-9">
                    <div>
                        <ul class="text-end mb-0">
                            <li class="list-unstyled d-inline-block" v-for="(nav, index) in navbar"> 
                                <a class="fw-semibold text-decoration-none" href="#">{{nav}}</a>
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
    header{
        z-index: 2;
        position: absolute;
        width: 100%;
        top: 0;
        padding: 23px 0 0;
        ul{
            li{                
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
                &:last-child{
                    a{
                        @include btn;
                        background-color: $first;
                        color: $second;
                    }
                }
            }
        }
    }
</style>