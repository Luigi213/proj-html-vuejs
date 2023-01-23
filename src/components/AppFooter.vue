<script>
export default {
    props:{
        navbar: Array
    }
}
</script>
<template lang="">
    <footer>
        <div class="container">
            <div class="row d-flex align-items-center">
                <div class="col-3">
                    <img src="../assets/images/footer-logo.png" alt="">
                </div>
                <div class="col-9">
                    <div>
                        <ul class="text-end mb-0">
                            <li class="list-unstyled d-inline-block" v-for="(nav, index) in navbar"> 
                                <a class="fw-bolder text-decoration-none text-black" href="#">{{nav}}</a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="col-12 my-3"><hr></div>
            </div>
            <div class="row">
                <div class="col-10">
                    <span>Copyright © 2022 <a class="text-decoration-none" href="#">Softivus</a>. All rights reserved.</span>
                </div>
                <div class="col-2">
                    <div class="icons text-end">
                        <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                        <a href="#"><i class="fa-brands fa-twitter"></i></a>
                        <a href="#"><i class="fa-brands fa-instagram"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>
<style lang="scss" scoped> 
    @use '../styles/partials/variables' as *;
    footer{
        .row{
            ul{
                li{
                    a{
                        font-size: 18px;
                    }
                    &:not(&:last-child){
                        margin-right: 23px;
                    }
                }
            }
            span{
                font-size: 18px;
                a{
                    color: $third
                }
            }
            .icons{
                a{
                    color: $third;
                    padding: 12px 15px;
                    border: 1px solid $sixth;
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
  
</style>