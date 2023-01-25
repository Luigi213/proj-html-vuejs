<script>
export default {
    
}
</script>
<template lang="">
    <section>
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="image-load d-flex align-items-center">
                        <img src="../assets/images/rocket-banner.png" alt="">
                    </div>
                </div>        
            </div>
        </div>
    </section>
</template>
<style lang="scss" scoped>
    section{
        position: relative;
        background: url('../assets/images/preloader.png');
        background-size: cover;
        .image-load{
            transform: translateY(10px) 3s linear infinite;
            width: 15vw ;
            margin: 0 auto;
            height: 100vh;
            img{
                animation: fly 3s linear infinite;
                @keyframes fly {
                    0%{
                        transform: translateX(0px);
                    }
                    50%{
                        transform: translateX(20px);
                    }
                    100%{
                        transform: translateX(0px);
                    }
                } 
            }
        }
    }
</style>