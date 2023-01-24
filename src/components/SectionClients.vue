<script>
export default {
    data(){
        return{
            sponsors:[
                {
                    img:'sponsor1.png',
                },
                {
                    img:'sponsor2.png',
                },
                {
                    img:'sponsor3.png',
                },
                {
                    img:'sponsor4.png',
                },
                {
                    img:'sponsor5.png',
                },
                {
                    img:'sponsor6.png',
                },
            ]
        }
    }
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
                <div class="col-2" v-for="(sponsor, index) in sponsors" :key="index">
                    <img :src="`src/assets/images/${sponsor.img}`" alt="sponsors">
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