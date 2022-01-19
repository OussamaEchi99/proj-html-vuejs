<template>
    <section>
        <div class="title">
            <span>CHOOSE YOUR FLAVOR</span>
            <h2>THE BEST PIZZA MENU IN THE TOWN</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ut blandit arcu in pretium molestie. interdum et malesuada fames ac.</p>
        </div>
        <div class="pizzas">
            <div v-for="(pizza, index) in pizzasMenusInfo" :key="index" class="pizza">
                <img :src="require(`../assets/img/h3-product-img-${pizza.img}a.png`)" :alt="pizza.name">
                <div class="details">
                    <span>{{ pizza.name }}</span>
                    <div class="price">
                        <span v-if="pizza.discount" class="discount">&#36;{{pizza.discount}}</span>
                        <span class="current_price">&#36;{{pizza.cost}}</span>
                        <span v-if="pizza.priceTo" class="price_to"> - &#36;{{pizza.priceTo}}</span>
                    </div>
                </div>
                <a v-if="pizza.sold" class="sold" href="#">SOLD</a>
            </div>
        </div>
        <a href="#" class="pizza_svg pizza_svg_grey"><img src="../assets/img/svg-4.svg" alt="Pizza Image"></a>
    </section>
</template>

<script>
export default {
    name: 'PizzaMenu',
    props: {
        pizzasMenusInfo: Array
    }
}
</script>

<style lang="scss" scoped>
@import '../style/Variables.scss';

section{
    position: relative;
    .title{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 300px;
        width: 27%;
        margin: auto;

        span{
            color: $brand_primary_color;
            font-size: 13px;
            font-weight: 500;
        }

        h2{
            margin: 5px 0 15px;
            font-weight: 500;
        }

        p{
            font-weight: 300;
            text-align: center;
        }
    }
    .pizzas{
        overflow-x: auto;
        display: flex;
        .pizza{
            width: 385px;
            display: flex;
            flex-direction: column;
            align-items: center;
            flex-shrink: 0;
            position: relative;

            img{
                width: 250px;
            }
            .details{
                display: flex;
                flex-direction: column;
                align-items: center;
                margin: 10px 0;
                text-transform: uppercase;

                > span{
                    color: $brand_tertiary_color;
                }

                .price{
                    color: $brand_primary_color;

                    .discount{
                        margin: 0 8px;
                        color: $brand_tertiary_color;
                        text-decoration: line-through;
                    }
                }
            }
            .sold{
                position: absolute;
                top: 0;
                right: 80px;
                padding: 20px 18px;
                background-color: $brand_primary_color;
                border-radius: 50%;
                color: white;
                font-size: 10px;
            }
        }
    }
    .pizza_svg{
        top: 210px
    }
}
</style>