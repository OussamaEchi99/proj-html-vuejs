<template>
    <main>
        <Banner />
        <Events :eventsImages="events" />
        <Proverbs />
        <Specials :specialsMenuDetails="specialsMenu"/>
        <BuildYourOwnPizza />
        <People />
        <BrandCollaboration :brandsImages="brands" />
        <PizzaMenu :pizzasMenusInfo="pizzasMenu"/>
    </main>
</template>

<script>
import Banner from "./Banner.vue";
import Events from "./Events.vue";
import Proverbs from "./Proverbs.vue";
import Specials from "./Specials.vue";
import BuildYourOwnPizza from "./BuildYourOwnPizza.vue";
import People from "./People.vue";
import BrandCollaboration from "./BrandCollaboration.vue";
import PizzaMenu from "./PizzaMenu.vue";

export default {
    name: 'Main',
    components: {
        Banner,
        Events,
        Proverbs,
        Specials,
        BuildYourOwnPizza,
        People,
        BrandCollaboration,
        PizzaMenu
    },
    data: function () {
        return {
            events: [
                {
                    img: '1'
                },
                {
                    img: '2'
                },
                {
                    img: '3'
                },
                {
                    img: '4'
                }
            ],
            specialsMenu: [
                {
                    title: 'Combo Piccolo',
                    cost: 10,
                    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent ut aliquam dui'
                },
                {
                    title: 'Combo Mezzo',
                    cost: 20,
                    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent ut aliquam dui'
                },
                {
                    title: 'Combo Grande',
                    cost: 30,
                    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent ut aliquam dui'
                }
            ],
            brands: [
                {
                    img: '1'
                },
                {
                    img: '2'
                },
                {
                    img: '3'
                },
                {
                    img: '4'
                },
                {
                    img: '5'
                }
            ],
            pizzasMenu: [
                {
                    img: '1',
                    name: 'Bismark',
                    cost: '30.00',
                    discount: '35.00',
                    sold: false
                },
                {
                    img: '2',
                    name: 'Fuori di zucca',
                    cost: '7.00',
                    priceTo: '50.00',
                    sold: false
                },
                {
                    img: '3',
                    name: 'Valdostana',
                    cost: '55.00',
                    sold: true
                },
                {
                    img: '4',
                    name: 'Pizza tartufata',
                    cost: '45.00',
                    sold: false
                },
                {
                    img: '5',
                    name: 'Francescana',
                    cost: '25.00',
                    sold: false
                },
                {
                    img: '6',
                    name: 'Campagnola',
                    cost: '5.00',
                    priceTo: '95.00',
                    sold: false
                }
            ],
        }
    }
}
</script>

<style lang="scss" scoped>

</style>