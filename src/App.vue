<script setup>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <Header @toggle-nav-bar="toggleNavBar" @toggle-dark-mode="toggleDarkMode" :darkMode="darkMode"/>
  <router-view :navBarIsActive="navBarIsActive" :darkMode="darkMode"></router-view>
  <Footer :darkMode="darkMode"/>
</template>

<script>
export default {
  name: 'App',
  props:{
    darkMode: Boolean,
  },
  components: {
    Header,
    Footer
  },
  data(){
    return {
      navBarIsActive: false,
      darkMode: false
      
    }
  },
  methods: {
    toggleNavBar(){
      this.navBarIsActive = !this.navBarIsActive;
    },
    toggleDarkMode(){
      this.darkMode = !this.darkMode;
      if(this.darkMode) {
        const body_tag_css = {
                              "background-color": "#142d4c",
                            }
        //Apply your CSS to the body tag.  You can enter any tag here, as
        //well as ID's and Classes.
        $("#app").css(body_tag_css);
      }else if(!this.darkMode) {
        const body_tag_css = {
                              "background-color": "#ececec",
                            }
        //Apply your CSS to the body tag.  You can enter any tag here, as
        //well as ID's and Classes.
        $("#app").css(body_tag_css);
      }
    }
  }
}

</script>


<style>

</style>
