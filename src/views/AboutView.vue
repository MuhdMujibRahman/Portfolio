<template>
  <div class="aboutContainer">
    <HomePage class="homePage"/>
    <div class="about">
    <h1>This is an about page</h1>
  </div>
  </div>

</template>

<script setup>
import HomePage from "@/components/HomePage.vue";
</script>

<script>
export default {
  name: "About",
  components: {
    HomePage
  },
}
</script>

<style scoped>
@keyframes slide-background {
  0%{left:127rem}
  
}
@keyframes slide-profile {
  0%{left:15rem;}
  
}
.aboutContainer{
  display:flex;
}
.homePage{
  left:-50rem;
  z-index:2;
  animation: slide-profile 1s ease-in-out;
  position: absolute;
}



.about {
  left:0;  
  width: 205.5vh;
  animation: slide-background 1s ease-in-out;
  background: #00204a;
  position: absolute;
  z-index: 1;
}




@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
