<template>
    <section>
        <div v-for="(brand, index) in brandsImages" :key="index" class="brand">
            <img :src="require(`../assets/img/h1-clients-img-${brand.img}.png`)" alt="Brand Logo">
        </div>
    </section>
</template>

<script>
export default {
    name: 'BrandsCollaboration',
    props: {
        brandsImages: Array
    }
}
</script>

<style lang="scss" scoped>
section{
    height: 300px;
    background-color: #f7f7f2;
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>