<script setup>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <Header @toggle-nav-bar="toggleNavBar"/>
  <router-view :navBarIsActive="navBarIsActive"></router-view>
  <Footer />
</template>

<script>
export default {
  name: 'App',
  components: {
    Header,
    Footer
  },
  data(){
    return {
      navBarIsActive: false,
    }
  },
  methods: {
    toggleNavBar(){
      this.navBarIsActive = !this.navBarIsActive;
    }
  }
}

</script>


<style>


</style>
