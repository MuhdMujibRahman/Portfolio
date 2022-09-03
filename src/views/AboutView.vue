<template>
  <div class="aboutContainer">
    <HomePage class="homePage"/>
    <div class="about">
      <div class="title">
        <h1>About me</h1>
      </div>
      <div class="aboutintro">
        <p>I am a Python developer with experience in API development using Flask and Django framework, building automated solution to support both strategic and tactical plans, which includes operations and engineering of my current company. I have experience in full-stack web development using Django, PorstgresSQL, Docker and Google Cloud Kubernetes Engine. Currently, I am looking into front-end web development such as Vuejs, SCSS and Nodejs.</p>
      </div>
    
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

.title{
  text-align: center;
  top:3rem;
  left:2.5rem;
  font-family: 'Oooh Baby', cursive;
  color: #428fe6;
  width: 100vh;
  font-size:1.5rem;
  font-weight:700;
}

.about {
  left:40rem;  
  width: 125vh;
  height: 25vh;
  animation: slide-background 1s ease-in-out;
  position: absolute;
  z-index: 1;
}

.aboutintro{
  top:8rem;
  left:-8rem;
  font-family: 'Roboto',sans-serif;
  font-size:2rem;
  font-weight: 10;
}




@media (min-width: 1024px) {
  .about {
    min-height: 70vh;
    display: flex;
  }
}
</style>
