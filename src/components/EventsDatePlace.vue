<template>
    <section>
        <div class="events_date_place">
            <div class="events">
                <div class="title">
                    <span>MADE WITH LOVE</span>
                    <h2>DELISH PIZZA DEALS</h2>
                </div>
                <ul>
                    <li v-for="(eventInfo, index) in eventsDatePlaceInfo" :key="index">
                        <div class="event">
                            <div class="date">
                            <h2>{{eventInfo.day}}</h2>
                            <h3>{{eventInfo.month}}</h3>
                            </div>
                            <ul>
                                <li class="details">
                                    <h3>{{eventInfo.nameEvent}}</h3>
                                    <span class="place">
                                        <i class="fas fa-map-marker-alt"></i>
                                        {{eventInfo.place}}
                                    </span>
                                </li>
                            </ul>
                        </div>
                        <div v-if="eventInfo.notLast" class="line"></div>
                    </li>
                </ul>
            </div>
        </div>
        <div class="comic_image">
            <img src="../assets/img/h3-img-5a.jpg" alt="Comics Image">
        </div>
        <a href="#" class="pizza_svg pizza_svg_grey up"><img src="../assets/img/svg-4.svg" alt="Pizza Image"></a>
        <a href="#" class="pizza_svg pizza_svg_grey down"><img src="../assets/img/svg-4.svg" alt="Pizza Image"></a>
    </section>
</template>

<script>
export default {
    name: 'EventsDatePlace',
    props: {
        eventsDatePlaceInfo: Array
    }
}
</script>

<style lang="scss" scoped>
@import '../style/Variables.scss';

section{
    display: flex;
    position: relative;
    margin: 8px 0;
    .events_date_place, .comic_image{
        width: calc(100% / 2);
    }

    .events_date_place{
        background-image: url('../assets/img/sky.png');
        height: 750px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        color: white;
        .events{
            width: 50%;
            margin: auto;
            font-weight: 500;
            text-transform: uppercase;
            > ul {
                > li{
                    margin-top: 40px;
                }
            }
            .title{
                margin-bottom: 20px;
                span{
                    color: $brand_primary_color;
                    font-size: 10px;
                }
            }
            .event{
                display: flex;
                ul{
                    margin: 0 40px;
                }
                .date{
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
                    align-items: center;
                    h2{
                        color: $brand_primary_color;
                        font-size: 45px;
                        line-height: 42px;
                    }
                    h3{
                        font-size: 25px;
                    }
                }
                .details{
                    h3{
                        font-size: 20px;
                    }
                    .place{
                        color: $brand_primary_color;
                        font-size: 10px;
                        text-transform: none;
                        i{
                            font-size: 15px;
                            margin-right: 5px;
                        }
                    }
                }
                
            }
            .line{
                border-bottom: 2px dotted $brand_tertiary_color;
                width: 100%;
                margin-top: 40px;
            }
        }
    }
    .up{
        top: 5px;
    }
    .down{
        bottom: 215px;
    }
}
</style>