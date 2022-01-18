<template>
    <main>
        <Banner />
        <Events :eventsImages="events" />
        <Proverbs />
    </main>
</template>

<script>
import Banner from "./Banner.vue";
import Events from "./Events.vue";
import Proverbs from "./Proverbs.vue";

export default {
    name: 'Main',
    components: {
        Banner,
        Events,
        Proverbs
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
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

</style>