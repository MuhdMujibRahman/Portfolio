<script setup>
import image from '@/assets/image/memoji.png'
import coffeMaker from '@/assets/image/coffee-maker.png'
import HomeDesktop from '../components/HomeDesktop.vue';
import HomeMobile from '../components/HomeMobile.vue';
import HomePage from '@/components/HomePage.vue';
</script>

<template>
  <!-- <HomeDesktop v-if="!mobileView"/> -->
  <HomeMobile :navBarIsActive="navBarIsActive" v-if="mobileView" :darkMode="darkMode"/>
  <HomePage/>
</template>

<script>
export default {
  name: 'Home',
  props: {
    navBarIsActive: Boolean,
    darkMode: Boolean
  },
  data (){
    return {
            mobileView: false,
            showHome: false
        };
  },
  methods: {
      handleViewChange() {
        this.mobileView = window.innerWidth <= 990;
      }
    },
    created(){
      this.handleViewChange();
    },
    components: { HomeDesktop, HomeMobile, HomePage}
}
</script>

<style scoped>



</style>
