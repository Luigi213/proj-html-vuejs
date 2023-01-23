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
            <div class="row">
                <div class="col-4">
                    <img src="../assets/images/logo.png" alt="">
                </div>
                <div class="col-8">
                    <div class="text-end">
                        <ul>
                            <li class="list-unstyled d-inline-block me-4" v-for="(nav, index) in navbar"> 
                                <a class="fw-bold text-white text-decoration-none" href="#">{{nav}}</a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    
    header{
        height: 400px;
        background: url('../assets/images/banner-bg.png') no-repeat center;
        background-size: cover;
        li{
            a{
                font-size: 18px;
            }
        }
    }
</style>