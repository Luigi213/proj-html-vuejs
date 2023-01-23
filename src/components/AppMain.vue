<script>
export default {

}
</script>
<template lang="">
    <main>
        <section class="jumbo">
            <div class="container">
                <div class="row">
                    <div class="col-12 text-center">
                        <h4>Imagine, Create, Experience</h4>
                        <h1 class="fw-semibold">We Animate <br> With Ninja-Like Precision</h1>
                        <p class="fs-5">We are a character-driven animation studio striving to make high-quality animations.</p>
                    </div>
                </div>
            </div>
            <div class="wave"></div>
        </section>
    </main>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    main{
        .jumbo{
            padding: 170px 0 0;
            margin-bottom: 200px;
            background: url('../assets/images/banner-bg.png') no-repeat center;
            background-size: cover;
            h4{
                color: $fifth;
            }
            h1{
                font-size: 70px ;
                color: $first
            }
            p{
                color: $first
            }
            .wave{
                height: 100%;
                background: url('../assets/images/bottom-shape.png') no-repeat bottom;
            }
        }
    }
</style>