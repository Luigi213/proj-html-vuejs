<script>
export default {
    
}
</script>
<template lang="">
    <section>
        <div class="container">
            <div class="row text-center">
                <div class="col-12">
                    <h4 class="fw-semibold">Why Anidio studio?</h4>
                    <h1 class="fw-semibold">We Love Our Clients</h1>
                    <p>We are trusted throughout adland and have a wealth of recommendations <br> from start-ups to renowned global brands.</p>
                </div>
            </div>
            <div class="row mt-5">
                <div class="col-2">
                    <img src="../assets/images/sponsor1.png" alt="sponsor1">
                </div>
                <div class="col-2">
                    <img src="../assets/images/sponsor2.png" alt="sponsor2">
                </div>
                <div class="col-2">
                    <img src="../assets/images/sponsor3.png" alt="sponsor3">
                </div>
                <div class="col-2">
                    <img src="../assets/images/sponsor4.png" alt="sponsor4">
                </div>
                <div class="col-2">
                    <img src="../assets/images/sponsor5.png" alt="sponsor5">
                </div>
                <div class="col-2">
                    <img src="../assets/images/sponsor6.png" alt="sponsor6">
                </div>
            </div>
        </div>
    </section>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    section{
        margin-top: 200px ;
        .container{
            .row{
                .col-12{
                    h4{
                        color: $third;
                    }
                    h1{
                        font-size: 60px;
                    }
                    p{
                        font-size: 18px;
                    }
                }
            }
        }
    }
</style>