<script setup>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <Header />
  <router-view></router-view>
  <Footer />
</template>

<style>


.container {
  margin: 25px;
  width: 100rem;
  height: 5rem;

  /* Setup */
  position: relative;
}

.navMenu {
  min-height: 0rem;
  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
}

.navMenu a {
  color: #142d4c;
  text-decoration: none;
  font-size: 1.2em;
  text-transform: uppercase;
  font-weight: 500;
  display: inline-block;
  width: 80px;
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  margin: 10px;
}

.navMenu a:hover {
  color: #9fd3c7;
}

.navMenu .dot {
  width: 6px;
  height: 6px;
  background: #9fd3c7;
  border-radius: 50%;
  opacity: 0;
  -webkit-transform: translateX(30px);
  transform: translateX(30px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
}

.navMenu a:nth-child(1):hover ~ .dot {
  -webkit-transform: translateX(35px);
  transform: translateX(35px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity: 1;
}

.navMenu a:nth-child(2):hover ~ .dot {
  -webkit-transform: translateX(136px);
  transform: translateX(136px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity: 1;
}

.navMenu a:nth-child(3):hover ~ .dot {
  -webkit-transform: translateX(236px);
  transform: translateX(236px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity: 1;
}

.navMenu a:nth-child(4):hover ~ .dot {
  -webkit-transform: translateX(340px);
  transform: translateX(340px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity: 1;
}

</style>
