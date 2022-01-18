<template>
    <main>
        <Banner />
        <Events :eventsImages="events" />
        <Proverbs />
        <Specials :specialsMenuDetails="specialsMenu"/>
        <BuildYourOwnPizza />
        <People />
    </main>
</template>

<script>
import Banner from "./Banner.vue";
import Events from "./Events.vue";
import Proverbs from "./Proverbs.vue";
import Specials from "./Specials.vue";
import BuildYourOwnPizza from "./BuildYourOwnPizza.vue";
import People from "./People.vue";

export default {
    name: 'Main',
    components: {
        Banner,
        Events,
        Proverbs,
        Specials,
        BuildYourOwnPizza,
        People
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
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

</style>