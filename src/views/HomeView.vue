<script setup>
import image from '@/assets/image/memoji.png'
import coffeMaker from '@/assets/image/coffee-maker.png'
import HomeDesktop from '../components/HomeDesktop.vue';
import HomeMobile from '../components/HomeMobile.vue';
</script>

<template>
  <HomeDesktop v-if="!mobileView"/>
  <HomeMobile v-if="mobileView"/>
</template>

<script>
export default {
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
    components: { HomeDesktop, HomeMobile}
}
</script>

<style scoped>



</style>
