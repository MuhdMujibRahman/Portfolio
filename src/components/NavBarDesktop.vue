<template>
    <div class="container">
      <nav class="navMenu">
        <router-link to="/">Home</router-link>
        <router-link to="">Blog</router-link>
        <router-link to="">About</router-link>
        <router-link to="">Work</router-link>
      <div class="dot"></div>
      </nav>
    </div>
</template>


<style scoped>
.container {
  margin: 25px;
  width: 100rem;
  height: 5rem;
  left:11.5rem;
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
  text-align: center ;
}

.navMenu a:hover {
  color: #d9faff;
  background: #00204a
}

.navMenu .dot {
  width: 6px;
  height: 6px;
  background: #005792;
  border-radius: 50%;
  opacity: 0;
  -webkit-transform: translateX(30px);
  transform: translateX(30px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
}

.navMenu a:nth-child(1):hover ~ .dot {
  -webkit-transform: translateX(45px);
  transform: translateX(45px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity: 1;
}

.navMenu a:nth-child(2):hover ~ .dot {
  -webkit-transform: translateX(150px);
  transform: translateX(150px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity: 1;
}

.navMenu a:nth-child(3):hover ~ .dot {
  -webkit-transform: translateX(245px);
  transform: translateX(245px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity: 1;
}

.navMenu a:nth-child(4):hover ~ .dot {
  -webkit-transform: translateX(350px);
  transform: translateX(350px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity: 1;
}

@media only screen and (min-width: 992px) and (max-width: 1200px){
  .container {
    margin: 25px;
    width: 100rem;
    height: 5rem;
    left:-12rem;
    /* Setup */
    position: relative;
}
}
</style>