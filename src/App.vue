<template>
  <div id="app">
    <Header :headerMenuLeft='header_menu_left' :headerMenuRight='header_menu_right' :headerCartSearchMenu='header_menu_cart_search'/>
    <Main />
    <Footer :locationsRestaurantInfo="locations" :workingHoursInfo="workingHours"/>
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
      ],
      locations: [
        {
          row: '1614E. Bell Rd #104',
          city: 'Salerno, AZ 85022',
          telephone: '(602)867-1010'
        },
        {
          row: '204 E. Pizzwtta Tommaso',
          city: 'Sorrento, AZ 85022',
          telephone: '(358)867-1010'
        },
        {
          row: 'Vale Puglia 54',
          city: 'Toore Del Greco AZ 85022',
          telephone: '(359)867-1010'
        },
        {
          row: 'Corso Itali AA',
          city: 'Naples, AZ 85022',
          telephone: '(989)867-1010'
        }
      ],
      workingHours: [
        {
          day: 'Monday',
          hour: 'Kitche Closed',
        },
        {
          day: 'Tuseday util Friday',
          hour: '9:00 - 22:00',
        },
        {
          day: 'Saturday',
          hour: 'Saturday 11am to midnight',
        },
        {
          day: 'Sunday',
          hour: '9:00 - 22:00',
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
