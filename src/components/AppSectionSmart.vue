<script>
export default {
    
}
</script>
<template lang="">
    <section class="Animetion">
        <div class="container">
            <div class="row">
                <div class="col-9 offset-3 text-center">
                    <div class="row">
                        <div class="col-10">
                            <h5 class="fw-semibold fs-4">Our Love For Animation</h5>
                            <h1 class="fw-semibold">We're Storytelling Experts With Creative Smarts</h1>
                            <p>Our culture inspires the creative and innovative spirit found throughout our Studio. We breathe life into new ideas!</p>                                
                        </div>                                            
                    </div>
                    <div class="row text-center">
                        <div class="col-4">
                            <div>
                                <img src="" alt="">
                                <h3>3D modeling</h3>
                            </div>
                        </div>
                        <div class="col-4">
                            <div>
                                <h3>3D modeling</h3>                                
                            </div>
                        </div>
                        <div class="col-4">
                            <div>                                
                                <h3>3D modeling</h3>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="smart">
            <img src="../assets/images/smart.png" alt="smarttwo">
        </div>
    </section>
</template>
<style lang="scss" scoped> 
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    .Animetion{
        padding-top: 130px ;
        position: relative;        
        .smart{            
            width: 500px;
            height: 900px;
            position: absolute;
            top:0;
            left: 0;
            img{
                width: 100%;
                height: 100%;
            }
        }
        .container{
            .row{
                h5{
                    color: $third;
                }
                h1{
                    font-size: 60px;
                }
                p{
                    width: 75%;
                    font-size: 17px ;
                    margin: 0 auto;
                }
            }
        }
    }
</style>