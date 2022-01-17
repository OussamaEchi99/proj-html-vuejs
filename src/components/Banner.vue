<template>
    <div class="banner">
        <div class="pizza_type_text">
            <img src="../assets/img/h3-rev-img-5.png" alt="Pizza Type Text">
            <div class="pizza_type_logo">
                <img src="../assets/img/h3-rev-img-6.png" alt="Pizza Type Logo">
            </div>
        </div>
        <span class="prev_slide slides_btn">PREV</span>
        <span class="next_slide slides_btn">NEXT</span>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>

.banner{
    height: 450px;
    background-image: url('../assets/img/sky.png');
    position: relative;

    .pizza_type_text{
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;

        img{
            width: 700px;
        }
        .pizza_type_logo{
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%,-50%);

            img{
                width: 260px;
            }
        }
    }
    .next_slide{
        right: -38px;
        transform: rotate(270deg);
    }
}
</style>