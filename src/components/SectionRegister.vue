<script>
export default {
    
}
</script>
<template lang="">
    <section>
        <div class="container">
            <div class="row text-center">
                <div class="col-12">
                    <h4 class="fw-semibold">We Create New Worlds!</h4>
                    <h1 class="fw-semibold">Want Tips On Your <br> Storytelling?</h1>
                    <p>Join our newsletter for tips on how to elevate your brand through storytelling</p>
                </div>
            </div>
            <div class="row justify-content-center">
                <div class="col-7">
                    <form action="#">
                        <input type="email" placeholder="Enter you email">
                        <button class="fw-semibold" type="sumbit">Sumbit</button>
                    </form>
                </div>
            </div>
        </div>
        <div class="shape-top">
            <img src="../assets/images/shape-top.png" alt="shape-top">
        </div>
        <div class="shape-bottom">
            <img src="../assets/images/shape-bottom.png" alt="shape-top">
        </div>
    </section>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    section{
        position: relative;
        background: url('../assets/images/counter-bg.png') no-repeat center;
        margin-top: 110px ;
        padding: 100px 0;
        .container{
            .row{
                .col-12{
                    h4{
                        color: $fifth;
                    }
                    h1{
                        font-size: 60px;
                        color: $first;
                    }
                    p{
                        font-size: 18px;
                        color: $first;
                    }
                }
                .col-7{
                    position: relative;
                    input{
                        width: 100%;
                        padding: 23px;
                        border-radius: 100px;
                    }
                    button{
                        font-size: 18px;
                        position: absolute;
                        top: 10px;
                        right: 26px;
                        padding: 13px 38px;
                        border-radius: 100px;
                        background-color: rgb(255, 223, 237);
                    }
                }
            }
        }
        .shape-top{
            position: absolute;
            top:0;
            left:0;
        }
        .shape-bottom{
            position: absolute;
            bottom: -0.1%;
        }
    }
</style>