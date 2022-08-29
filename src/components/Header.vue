<template>
<header>
  <NavBarMobile id="navigation-icon" v-if="mobileView"/>
  <NavBarDesktop v-if="!mobileView"/>
</header>
</template>

<script>
import NavBarDesktop from './NavBarDesktop.vue';
import NavBarMobile from './NavBarMobile.vue';
  export default {
    data() {
        return {
            mobileView: false,
            showNavBar: false
        };
    },
    methods: {
      handleViewChange() {
        console.log(window.innerWidth)
        console.log(window.innerWidth <= 990)
        this.mobileView = window.innerWidth <= 990;
      }
    },
    components: { NavBarDesktop, NavBarMobile },
    created(){
      this.handleViewChange();
    }
}
</script>

<style scoped>
#navigation-icon {
  padding: 10px 10px 20px;
  margin-right: 10px;
  cursor: pointer;
}

#navigation-icon > i {
  font-size: 2rem;
}
</style>
