<template>
  <div id="app">
    <Header :headerMenuLeft='header_menu_left' :headerMenuRight='header_menu_right' :headerCartSearchMenu='header_menu_cart_search'/>
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer
  },
  data: function () {
    return {
      header_menu_left: [
        {
          text: 'Home',
          img: 'svg-0.svg'
        },
        {
          text: 'Pages'
        },
        {
          text: 'Menu'
        },
      ],
      header_menu_right: [
        {
          text: 'Event'
        },
        {
          text: 'Blog'
        },
        {
          text: 'Landing'
        }
      ],
      header_menu_cart_search: [
        {
          img: 'svg-1.svg',
          text: 'Cart',
          value: true
        },
        {
          img: 'search-solid.svg',
          text: 'Search',
          value: false
        }
      ]
    }
  }
};
</script>

<style lang="scss">
@import './style/General.scss';
@import './style/Common.scss';
@import './style/Variables.scss';

</style>
