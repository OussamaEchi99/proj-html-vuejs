<template>
    <footer>
        <div class="info_section">
            <div class="footer_details">
                <div class="locations">
                    <h3>FIND OUR RESTAURANTS</h3>
                    <ul>
                        <li v-for="(location, index) in locationsRestaurantInfo" :key="index" class="location">
                            <span>{{location.row}}</span>
                            <span>{{location.city}}</span>
                            <span>{{location.telephone}}</span>
                        </li>
                    </ul>
                    <span class="user_created">Created with <i class="far fa-heart"></i> by <a href="#">Qode Interactive</a></span>
                </div>
                <div class="opening_days">
                    <h3>WORKING HOURS</h3>
                    <ul>
                        <li v-for="(infoDays, index) in workingHoursInfo" :key="index" class="day">
                            <h5>{{infoDays.day}}</h5>
                            <span class="close">{{infoDays.hour}}</span>
                        </li>
                        <li class="socials">
                            <h3>FOLLOW US:</h3>
                            <span><i class="fab fa-twitter"></i></span>
                            <span><i class="fab fa-facebook-f"></i></span>
                            <span><i class="fab fa-instagram-square"></i></span>
                            <span><i class="fab fa-linkedin-in"></i></span>
                        </li>
                    </ul>
                </div>
                <div class="phrase">
                    <h2>THE DON PEPPE CREW FIRST AND FOREMOST VALUES AN AUTHENTIC. WELL BAKED SLICE OF PIZZA</h2>
                </div>
            </div>
        </div>
        <div class="footer_image">
            <img src="../assets/img/footer-img-1.jpg" alt="Footer Image">
            <a href="#" class="pizza_svg pizza_svg_grey"><img src="../assets/img/svg-4.svg" alt="Pizza Image"></a>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
    props: {
        locationsRestaurantInfo: Array,
        workingHoursInfo: Array
    }
}
</script>

<style lang="scss" scoped>
@import '../style/Variables.scss';

footer{
    display: flex;
    color: #9b9b9b;
    font-weight: 500;
    .info_section, .footer_image{
        width: calc(100% / 2);
    }

    .footer_image{
        position: relative;
        .pizza_svg{
            bottom: 40px;
        }
    }

    .info_section{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        background-image: url('../assets/img/sky.png');
    }

    .footer_details{
        display: flex;
        justify-content: space-evenly;
        .locations{
            position: relative;
            width: 24%;
            h3{
                color: $brand_tertiary_color;
                font-weight: 500;
            }
            .location{
                display: flex;
                flex-direction: column;
                font-size: 14px;
                margin: 15px 0 20px;
                font-weight: 300;
            }
            .user_created{
                color: $brand_tertiary_color;
                position: absolute;
                left: 0;
                bottom: -130px;
                a{
                    color: #2c7a53;
                }
            }
        }
        .opening_days{
            *{
                font-weight: 500;
            }

            h3{
                color: $brand_tertiary_color;
            }

            ul{
                li:first-child{
                    span{
                        color: #a0351c;
                    }
                }

                li{
                    font-size: 14px;
                    margin: 15px 0;
                }
            }

            .day{
                h5{
                    color: $brand_tertiary_color;
                    font-size: 14px;
                }
            }
            .socials{
                display: flex;
                span{
                    margin: 0 10px;
                    color: white;
                }
            }
        }
        .phrase{
            width: 30%;
            color: white;
        }
    }

    .footer_image{
        img{
            height: 100%;
            object-fit: cover;
        }
    }
}
</style>