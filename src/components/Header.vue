<template>
<header>
  <NavBarMobile 
  @nav-click="$emit('toggle-nav-bar')"
  @darkmode-click="$emit('toggle-dark-mode')"
  :darkMode="darkMode"
  id="navigation-icon" v-if="mobileView"/>
  <NavBarDesktop v-if="!mobileView"/>
</header>
</template>

<script>
import NavBarDesktop from './NavBarDesktop.vue';
import NavBarMobile from './NavBarMobile.vue';
  export default {
    emits: ['toggle-nav-bar','toggle-dark-mode'],
    props: {
      darkMode: Boolean
    },
    data() {
        return {
            mobileView: false,
            showNavBar: false
        };
    },
    methods: {
      handleViewChange() {
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
