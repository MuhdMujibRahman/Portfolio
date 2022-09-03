<script setup>
  import HomePage from "@/components/HomePage.vue";
  import ExperiencePage from "@/components/ExperiencePage.vue";
import LanguageAndTools from "../components/LanguageAndTools.vue";
</script>

<template>
  <div class="aboutpage">
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
    <div class="bottompage">
      <ExperiencePage/> 
      <LanguageAndTools/>
    </div>
    
    
  </div>


</template>

<script>
export default {
  name: "About",
  components: {
    HomePage,
    ExperiencePage,
    LanguageAndTools
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
.bottompage {
  display: grid;
}
.aboutpage{
  min-height:200vh;
  display: block;
}
.aboutContainer{
  display:block;
}
.homePage{
  left:-50rem;
  animation: slide-profile 1s ease-in-out;
  position: absolute;
}

.title{
  font-family: 'Oooh Baby', cursive;
  color: #428fe6;
  width: 100vh;
  font-size:1.5rem;
  font-weight:700;
}

.about {
  top:5rem;
  left:50rem;  
  width: 80vh;
  height: 25vh;
  animation: slide-background 1s ease-in-out;
  position: absolute;

}

.aboutintro{
  font-family: 'Roboto',sans-serif;
  font-size:2rem;
  font-weight: 10;
}




/* @media (min-width: 1024px) {
  .about {
    min-height: 100vh;
  }
} */
</style>
