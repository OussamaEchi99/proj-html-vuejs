<template>
    <main>
        <Banner />
        <Events :eventsImages="events" />
    </main>
</template>

<script>
import Banner from "./Banner.vue";
import Events from "./Events.vue";

export default {
    name: 'Main',
    components: {
        Banner,
        Events
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