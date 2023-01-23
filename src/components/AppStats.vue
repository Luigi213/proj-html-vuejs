<script>
export default {
    
}
</script>
<template lang="">
    <section>
        <div class="container">
            <div class="row text-center">
                <div class="col-12 mb-5">
                    <h1 class="fw-semibold">Anidio Quick Facts</h1>
                </div>
                <div class="col-3">
                    <div class="stats">
                        <h2 class="fw-semibold">700+</h2>
                        <p>Projects done</p>
                    </div>
                </div>
                <div class="col-3">
                    <div class="stats">
                        <h2 class="fw-semibold">250+</h2>
                        <p>Happy Clients</p>
                    </div>
                </div>
                <div class="col-3">
                    <div class="stats">
                        <h2 class="fw-semibold">25+</h2>
                        <p>Team Members</p>
                    </div>
                </div>
                <div class="col-3">
                    <div class="stats">
                        <h2 class="fw-semibold">12+</h2>
                        <p>Years on the market</p>
                    </div>
                </div>
            </div>
        </div>
        <div class="shape-top">
            <img src="../assets/images/shape-top.png" alt="shape-top">
        </div>
        <div class="shape-bottom">
            <img src="../assets/images/shape-bottom.png" alt="shape-top">
        </div>
        <div class="globe">
            <img src="../assets/images/globe.png" alt="">
        </div>
    </section>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    section{
        background: url('../assets/images/counter-bg.png') no-repeat center;
        position: relative;
        padding: 100px 0;
        .stats, h1{
            color: $first;
        }
        h1{
            position: relative;
            font-size: 60px;
            z-index: 2;
        }
        .stats{
            position: relative;
            z-index: 3;
            padding: 30px 0;
            border: 1px solid $sixth;
            border-radius: 20px;
            transition: all 0.3s;
            &:hover{
                transform: skewY(5deg);
            }
            h2{
                font-size: 60px;
            }
            p{
                color: $fifth;
            }
        }
        .shape-top, .shape-bottom, .globe{
            position: absolute;
            z-index: 1;
        }
        .shape-top{
            top:0;
            left:0;
        }
        .shape-bottom{
            bottom:0;
        }
        .globe{
            height: 95%;
            position: absolute;
            z-index: 0;
            left: 34%;
            top: 2.4%;
            animation: spin 10s linear infinite;
            @keyframes spin {
                0%{
                    transform: rotate(0deg);
                }
                100%{
                    transform:rotate(360deg);
                }
            }
            img{
                height: 100%;
            }
        }
    }
</style>