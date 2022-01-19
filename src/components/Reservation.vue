<template>
    <section>
        <img src="../assets/img/h3-background-img-3.jpg" alt="Background Image">
        <div class="inputs_section">
            <div class="inputs">
                <div class="input">
                    <input type="text" placeholder="1 person">
                    <span><i class="fas fa-user-friends"></i></span>
                </div>
                <span>FOR</span>
                <div class="input">
                    <input type="text" placeholder="11/29/2020">
                    <span><i class="far fa-calendar"></i></span>
                </div>
                <span>AT</span>
                <div class="input">
                    <input type="text" placeholder="7:00 pm">
                    <span><i class="far fa-clock"></i></span>
                </div>
                <a class="primary_btn" href="#">BOOK A TABLE</a>
            </div>
            <span>&ast;Powered by OpenTable</span>
        </div>
    </section>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
@import '../style/Variables.scss';

section{
    position: relative;
    .inputs_section{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%,-50%);
        .inputs{
            margin-bottom: 10px;
            display: flex;
            align-items: center;

            .input{
                position: relative;

                i{
                    position: absolute;
                    right: 10px;
                    top: 50%;
                    transform: translate(-50%,-50%);
                    color: $brand_tertiary_color;
                }
            }

            input{
                height: 60px;
                padding: 0 20px;
                width: 250px;
                border: 2px solid black;
            }

            > span{
                color: white;
                margin: 0 20px;
            }

            .primary_btn{
                display: flex;
                justify-content: center;
                align-items: center;
                width: 250px;
                height: 60px;
                margin-left: 50px;
                font-size: 12px;
            }
        }
        > span {
            color: white;
            font-weight: 300;
            margin-top: 20px;
        }
    }
}
</style>