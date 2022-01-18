<template>
    <section>
        <img src="../assets/img/h3-testimonials-bckgrnd.jpg" alt="">
        <div class="phrase">
            <h2>&ldquo;</h2>
            <p>&ldquo;Forget the trendy pizza shops, this hidden spot makes the best new york-style pizza slice in Naples&rdquo;</p>
            <span>Washington post 2018</span>
            <div class="slides_points">
                <div class="slide_point active"></div>
                <div class="slide_point"></div>
                <div class="slide_point"></div>
            </div>
        </div>
        <span class="prev_slide slides_btn">PREV</span>
        <span class="next_slide slides_btn">NEXT</span>
        <a href="#" class="pizza_svg pizza_svg_grey"><img src="../assets/img/svg-4.svg" alt="Pizza Image"></a>
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
        font-weight: bold;
        text-transform: uppercase;
        .phrase {
            display: flex;
            flex-direction: column;
            align-items: center;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%,-50%);

            h2{
                font-size: 130px;
                color: $brand_tertiary_color;
            }

            p{
                font-size: 31px;
                text-align: center;
                color: $brand_secondary_color;
                margin-top: -70px;
            }

            > span{
                color: $brand_primary_color;
                margin: 10px 0 15px;
            }

            .slides_points{
                display: flex;
                .slide_point{
                    padding: 5px;
                    background-color: #e4e4d4;
                    border-radius: 50%;
                    margin: 0 5px;

                    &.active{
                        background-color: $brand_tertiary_color;
                    }
                }
            }
        }
        .pizza_svg{
            bottom: 40px;
        }
    }
</style>