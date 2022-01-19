<template>
    <section>
        <div v-for="(event, index) in eventsImages" :key="index" class="event_image">
            <img :src="require(`../assets/img/h3-img-${event.img}.jpg`)" :alt="`Image ${event.img}`">
            <a href="#" class="image_hover">
                <img src="../assets/img/poits_background.jpg" alt="Hover Image">
                <a class="primary_btn" href="#">
                    <i class="far fa-eye"></i>
                </a>
            </a>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Events',
    props: {
        eventsImages: Array
    }
}
</script>

<style lang="scss" scoped>
    section{
        display: flex;
        justify-content: space-between;
        flex-shrink: 0;
        margin: 8px 0;

        .event_image{
            width: calc((100% / 4) - 5px);
            position: relative;
            overflow: hidden;

            > img{
                height: 100%;
                object-fit: cover;
            }

            img{
                width: 100%;
            }

            .image_hover{
                position: absolute;
                display: none;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                width: 100%;
                height: 100%;
                transition: 0.5s ease;

                a{
                    position: absolute;
                    top: 50%;
                    left: 50%;
                    transform: translate(-50%,-50%);
                    z-index: 2;
                    font-size: 25px;
                    padding: 25px 27px;
                    border-radius: 50%;
                }
            }

            &:hover .image_hover{
                display: block;
            }
        }
    }
</style>