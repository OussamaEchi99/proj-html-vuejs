<template>
    <section>
        <div class="col">
            <img src="../assets/img/h1-img-4.jpg" alt="Pizza Specials Image">
            <div class="pizza_specials_logo">
                <img src="../assets/img/h1-img-7n.png" alt="Pizza Specials Logo">
            </div>
        </div>
        <div class="col pizzas_specials_products">
            <div class="pizza_specials_menu">
                <h2>SPECIALS&#42;</h2>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. <br> Praesent ut.</p>
                <ul>
                    <li v-for="(menuDetail, index) in specialsMenuDetails" :key="index" class="menu">
                        <span>${{ menuDetail.cost }}</span>
                        <ul class="description">
                            <li>
                                <span>{{ menuDetail.title }}</span>
                                <p>{{ menuDetail.description }}</p>
                            </li>
                        </ul>
                    </li>
                </ul>
            </div>
            <a href="#" class="pizza_svg pizza_svg_grey"><img src="../assets/img/svg-4.svg" alt="Pizza Image"></a>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Specials',
    props: {
        specialsMenuDetails: Array
    }
}
</script>

<style lang="scss" scoped>
@import '../style/Variables.scss';

    section{
        display: flex;
        .col{
            width: calc(100% / 2);
            margin: 5px 0;
            position: relative;

            .pizza_specials_logo{
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%,-50%);
            }
        }
        
        .pizzas_specials_products{
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;

            .pizza_specials_menu{
                width: 42%;
                margin: auto;

                h2{
                    font-size: 40px;
                }
                .menu{
                    display: flex;
                    margin: 17px 0;
                    > span{
                        color: $brand_primary_color;
                        font-weight: bold;
                        font-size: 26px;
                    }
                    .description{
                        margin-left: 15px;
                        span{
                            text-transform: uppercase;
                            font-weight: 500;
                            font-size: 26px;
                        }
                        p{
                            font-size: 13px;
                        }
                    }
                }
            }

            .pizza_svg{
                bottom: 175px;
            }
        }
    }
</style>