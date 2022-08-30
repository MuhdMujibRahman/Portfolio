<script setup>
import github from '@/assets/image/github-logo.png'
import githubInvert from '@/assets/image/github.png'
import linkedin from '@/assets/image/linkedin.png'
import linkedInvert from '@/assets/image/linkedin_2.png'
</script>
<template>
    <footer>
        <ul class="wrapper">
            <li class="icon linkedin">
              <a target="_blank" href="https://www.linkedin.com/in/mujibnizar/">
                <span class="tooltip">Linkedin</span>
                <span>
                  <img 
                  @mouseover="hoverEventLinkedin"
                  @mouseleave="hoverEventLinkedin"
                  v-show="!hoverLinkedin"
                  class="icon linkedin" 
                  :src="linkedin" 
                  href="https://www.linkedin.com/in/mujibnizar/">
                  
                  <img  @mouseover="hoverEventLinkedin"
                        @mouseleave="hoverEventLinkedin" 
                        v-show="hoverLinkedin"
                        class="icon linkedin" 
                        :src="linkedInvert" 
                        href="https://www.linkedin.com/in/mujibnizar/">
                </span>
              </a>

            </li>
            <li class="icon github">
              <a target="_blank" href="https://github.com/MuhdMujibRahman">
                <span class="tooltip">Github</span>
                <span><img 
                  @mouseover="hoverEventGit"
                  @mouseleave="hoverEventGit"
                  v-show="!hoverGit"
                  class="icon github" :src="github">
                  <img @mouseover="hoverEventGit"
                        @mouseleave="hoverEventGit" 
                        v-show="hoverGit"
                        class="icon github" :src="githubInvert"></span>
  
              </a>

            </li>
        </ul>
        <p :class="{darkmode: darkMode}">Copyright &copy; 2022</p>
        <ul>
        <li class="credit" :class="{darkmode: darkMode}">
            <a href="https://www.flaticon.com/free-icons/coffee-maker" title="coffee maker icons">Coffee maker icons created by flatart_icons - Flaticon</a>
        </li>
        <li class="credit" :class="{darkmode: darkMode}">
            <a href="https://www.flaticon.com/free-icons/cat" title="cat icons">Cat icons created by Dave Gandy - Flaticon</a>
        
        </li>
        <li class="credit" :class="{darkmode: darkMode}">
            <a href="https://www.flaticon.com/free-icons/linkedin" title="linkedin icons">Linkedin icons created by Freepik - Flaticon</a>
        </li>
        </ul>

    </footer>
</template>

<script>

export default {
  props : {
    darkMode : Boolean,
  },
    data () {
        return {
            github: github,
            linkedin: linkedin,
            linkedInvert: linkedInvert,
            githubInvert: githubInvert,
            hoverGit: false,
            hoverLinkedin: false,
        }
    },
    methods: {
      hoverEventGit(){
        this.hoverGit = !this.hoverGit;
      },
      hoverEventLinkedin(){
        this.hoverLinkedin = !this.hoverLinkedin;
      }
    }
}

</script>

<style scoped>

p.darkmode{
  color: #e3e3e3;
}

a{
    color: #333;
}

footer{
    margin-top: auto;
    text-align: center;
}


* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

*:focus,
*:active {
  outline: none !important;
  -webkit-tap-highlight-color: transparent;
}

html,
body {
  display: grid;
  height: 100%;
  width: 100%;
  font-family: "Poppins", sans-serif;
  place-items: center;
  background: linear-gradient(315deg, #ffffff, #d7e1ec);
}

.wrapper {
  display: inline-flex;
  list-style: none;
}

.wrapper .icon {
  position: relative;
  background: #ffffff;
  border-radius: 50%;
  padding: 15px;
  margin: 10px;
  width: 50px;
  height: 50px;
  font-size: 18px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  box-shadow: 0 10px 10px rgba(0, 0, 0, 0.1);
  cursor: pointer;
  transition: all 0.2s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}
.githubInverted {
  display: none;
}
.linkedinInverted {
  display: none;
}
.wrapper .tooltip {
  position: absolute;
  top: 0;
  right: -0.1rem;
  font-size: 14px;
  background: #ffffff;
  color: #ffffff;
  padding: 5px 8px;
  border-radius: 5px;
  box-shadow: 0 10px 10px rgba(0, 0, 0, 0.1);
  opacity: 0;
  pointer-events: none;
  transition: all 0.3s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

.wrapper .tooltip::before {
  position: absolute;
  content: "";
  height: 8px;
  width: 8px;
  background: #ffffff;
  bottom: -3px;
  left: 50%;
  transform: translate(-50%) rotate(45deg);
  transition: all 0.3s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

.wrapper .icon:hover .tooltip {
  top: -45px;
  opacity: 1;
  visibility: visible;
  pointer-events: auto;
}

.wrapper .icon:hover span,
.wrapper .icon:hover .tooltip {
  text-shadow: 0px -1px 0px rgba(0, 0, 0, 0.1);
}

.wrapper .linkedin:hover,
.wrapper .linkedin:hover .tooltip,
.wrapper .linkedin:hover .tooltip::before {
  background: #1877F2;
  color: #ffffff;
}



.wrapper .github:hover,
.wrapper .github:hover .tooltip,
.wrapper .github:hover .tooltip::before {
  background: #333333;
  color: #ffffff;
}


.icon > .github {
    height: 20px;
    width: 20px;
}
.icon > .linkedin {
    height: 20px;
    width: 20px;
}

@media (max-width: 480px) {
  li.credit {
    display: none;
  }
  .wrapper {
  left: 0.2rem;
  }

  p {
    width: 100%;
  }
}
</style>