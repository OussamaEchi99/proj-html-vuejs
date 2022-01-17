<template>
    <header>
        <div class="container">
            <div class="order_btn">
                <a class="primary_btn" href="#">ORDER ONLINE</a>
            </div>
            <div class="menu_logo">
                <ul>
                    <li v-for="(textMenu, index) in headerMenuLeft" :key="index">
                        <a href="#">
                            <img v-if="textMenu.img" :src="require(`../assets/img/${textMenu.img}`)" :alt="textMenu.text">
                            {{ textMenu.text }}
                        </a>
                    </li>
                    <li class="logo"><img src="../assets/img/h5-logo-divided-header.png" alt="Logo Image"></li>
                    <li v-for="(textMenu, index) in headerMenuRight" :key="index">
                        <a href="#">
                            {{ textMenu.text }}
                        </a>
                    </li>
                </ul>
            </div>
            <div class="cart_search_menu">
                <ul>
                    <li v-for="(textMenuCartSearch, index) in headerCartSearchMenu" :key="index">
                        <a href="#">
                            <img class="svg_invert" :src="require(`../assets/img/${textMenuCartSearch.img}`)" alt="">
                            {{ textMenuCartSearch.text }}
                            <span v-if="textMenuCartSearch.value" class="cart_number">0</span>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header',
    props: {
        headerMenuLeft: Array,
        headerMenuRight: Array,
        headerCartSearchMenu: Array
    }
}
</script>

<style lang="scss" scoped>
@import '../style/Variables.scss';

    header{
        height: 125px;
        background-image: url('../assets/img/sky.png');
        font-size: 12px;
        color: white;

        a{
            text-transform: uppercase;
            font-weight: bold;
        }

        .container{
            height: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;

            .order_btn{
                a{
                    padding: 15px 30px;
                }
            }
            
            .menu_logo{
                ul{
                    display: flex;
                    align-items: center;

                    .logo{
                        width: 140px;
                    }

                    a{
                        margin: 0 20px;
                        display: flex;

                        img{
                            filter: invert(1);
                            width: 16px;
                            margin-right: 5px;
                        }
                    }
                }
            }

            .cart_search_menu{
                ul{
                    display: flex;
                    align-items: center;
                    li{
                        display: flex;
                        align-items: center;
                        margin: 0 10px;
                        a{
                            display: flex;
                            align-items: center;
                            position: relative;

                            .cart_number{
                                position: absolute;
                                top: -7px;
                                left: -6px;
                                font-size: 7px;
                                padding: 3px 6px;
                                background-color: white;
                                border-radius: 50%;
                                color: $brand_primary_color;
                            }
                        }
                        img{
                            width: 20px;
                            margin-right: 5px;
                        }
                    
                    }
                }
            }
        }
    }
</style>