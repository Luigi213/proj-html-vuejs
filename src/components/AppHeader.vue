<script>
export default {
    props:{
        navbar: Array
    }
}
</script>
<template lang="">
    <header>
        <div class="container">
            <div class="row d-flex align-items-center">
                <div class="col-3">
                    <img src="../assets/images/logo.png" alt="">
                </div>
                <div class="col-9">
                    <div>
                        <ul class="text-end mb-0">
                            <li class="list-unstyled d-inline-block" v-for="(nav, index) in navbar"> 
                                <a class="fw-bolder text-decoration-none" href="#">{{nav}}</a>
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
    
    header{
        position: fixed;
        width: 100%;
        top: 0;
        padding-top: 23px;
        ul{
            li{                
                a{
                    font-size: 18px;
                    color: $first;
                }
                &:not(&:last-child){
                    margin-right: 20px;
                }
                &:last-child{
                    a{
                        padding: 13px 38px;
                        border-radius: 100px;
                        background-color: $first;
                        color: $second;

                    }
                }
            }
        }
    }
</style>