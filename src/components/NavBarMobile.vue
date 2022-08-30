<script setup>
import ToggleDarkMode from '@/components/ToggleDarkMode.vue'
</script>

<template>
        <div id="menu-icon">
		<a href="#" id="nav-toggle" 
        :class="{ active: isActive, darkmode: darkMode }"
        @click="isActive = !isActive, 
        showNavBar = !showNavBar"
		v-on:click="$emit('nav-click')"><span></span></a>
		</div>
        <transition name="fade" mode="out-in">
            <div id="nav" :class="{ active : showNavBar}">
            <nav class="navMenu" :class="{ active : showNavBar}">
                <a class="menu"><router-link to="/">Home</router-link></a>
                <a class="menu"><router-link to="">Blog</router-link></a>
                <a class="menu"><router-link to="">About</router-link></a>
            <div class="dot"></div>
            </nav>
        
		</div>
        </transition>
		<ToggleDarkMode @darkMode-btn="$emit('darkmode-click')"/>
</template>

<script>

export default {
	name: 'NavBarMobile',
	emits:['nav-click','darkmode-click'],
	props:{
		darkMode: Boolean
	},
	components: {
		ToggleDarkMode
	},
    data(){
        return {
            showNavBar: false,
            isActive: false,
            menuActive:false,
        }
    },
    methods:{
        toggleNavBar(){
            this.showNavBar = !this.showNavBar;
        }
    },
//     mounted(){
//         $(document).ready(function() {
// 				$('#nav-toggle').click(function(event) {
// 					$(this).toggleClass('active');
// 					if ($('#nav-toggle').hasClass('active')) 
// 					{
// 						$('#nav').show();
// 					} 
// 					else
// 					{
// 						$('#nav').hide();
// 					};
// 				});
// });
//     }
}

</script>

<style scoped>
body{
	background: #1E1E1E;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 20s;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}
.navMenu {
  display: block;
  min-height: 0rem;
  position: absolute;
  width: 150px;
  top: 10rem;
  left: 4rem;
  /* -webkit-transform: translate(-50%, -50%); */
  transform: translate(-50%, -50%);
}

/* a.menu{
    display: block;
    width: 100px;
  height: 100px;
  padding: 5px;
  border: 1px solid blue;    
  background-color: yellow; 
} */

.navMenu a {
  color: #142d4c;
  text-decoration: none;
  font-size: 1.2em;
  text-transform: uppercase;
  font-weight: 500;
  display: inline-block;
  width: 80px;
  margin: 10px;
}

a.menu > a:hover {
  color: #9fd3c7;
}

/* .navMenu .dot {
  width: 6px;
  height: 6px;
  background: #9fd3c7;
  border-radius: 50%;
  opacity: 0;
  -webkit-transform: translateX(30px);
  transform: translateX(30px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
} */

#nav.active > .navMenu.active > a.menu:nth-child(1) {
  /* -webkit-transform: translateX(35px);
  transform: translateX(35px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity: 1; */
  transition: left .5s, opacity .5s .1s;
}

#nav.active > .navMenu.active > a.menu:nth-child(2){
  /* -webkit-transform: translateX(136px);
  transform: translateX(136px); */
  transition: left 1.5s, opacity 1.5s 1.1s;
}

#nav.active > .navMenu.active > a.menu:nth-child(3) {
  /* -webkit-transform: translateX(236px);
  transform: translateX(236px); */
  transition: left 10s, opacity 2.5s 2.1s;
}




#nav{
    transition: opacity 9s ease-out;
    opacity: 10;
}

#nav.active{
    transition: opacity 9s ease-in;
    opacity: 10;
}

#nav-toggle{
	position: absolute;
	cursor: pointer;
	/* background: #142d4c;; */
	padding: 27px 50px 33px 12px;
	/* border: 5px solid #385170; */
	border-radius: 100%;
	display: none;
}
#nav-toggle span , #nav-toggle span:before , #nav-toggle span:after{
	position: absolute;
	content: '';
	display: block;
	background: #142d4c;
	width: 30px;
	height: 7px;
	border-radius: 1px;
	transition: all 500ms ease;
}
#nav-toggle.darkmode span , #nav-toggle.darkmode span:before , #nav-toggle.darkmode span:after{

	background: #9fd3c7;

}
#nav-toggle span:before{
	top: -10px;
}
#nav-toggle span:after{
	bottom: -10px;
}
#nav-toggle.active span:before, #nav-toggle.active span:after {
  top: 0;
}
#nav-toggle.active span{
	background: transparent;
}
#nav-toggle.active span:before{
	transform: rotate(45deg);
}
#nav-toggle.active span:after{
	transform: rotate(-45deg);
}
ul#navbar{
	list-style-type: none;
}
ul#navbar li{
	display: inline-block;
	font-size: 1.5em;
}
ul#navbar li a{
	text-decoration: none;
	display: block;
	padding: 10px;
	color: #9fd3c7;
	font-family: 'Roboto','Helvetica';
	background:#142d4c;
	transition: all 1s ease;
}
ul#navbar li a:hover{
	color: #ffffff;
	background: #9fd3c7;
}
@media only screen and (max-width: 480px) and (min-width: 381px){

.box {
  margin-top: 9rem;
  display: grid;
  position: relative;
  grid-template-columns: auto auto auto;
  width: fit-content;
  height: 20rem;
  border-left-width: 100rem;
  left:-30.9rem;
  gap: 20px;


}
}
@media (max-width: 480px){
	#nav-toggle.active{
		position: absolute;
		animation:rise 0.3s ease-in-out;
		top: 11%;
	}
	#nav-toggle{
		top: 40%;
		left: 5%;
		animation:drop 1s ease-in-out;
		display: block;
	}
    #nav.active{
    transition: left .7s ease-in;
    left: 1rem;
    }

    #nav.active > .menu {
        left: 0rem;
    }
    #nav.active > .navMenu.active >.menu a:nth-child(1){
        transition: left 0.1s ease-in-out;
    }
    #nav.active > .menu:nth-child(2){
        transition: left 1.5s ease-in-out;
    }
    #nav.active > .menu:nth-child(3){
        transition: left 10s ease-in-out;
    }

	#nav {
    transition: left 1s ease-in-out;
    left: -13rem;
    }

	ul#navbar{
		margin-top: 50px;
		padding-left: 0;
	}
	ul#navbar li{
		display: block;
	}
	ul#navbar li a{
		text-align: center;
	}

}
@media (min-width: 481px) and (max-width: 767px){
	.navMenu {
		display: flex;
		min-height: 0rem;
		position: absolute;
		width: 150px;
		top: 1.7rem;
		left: 16.5rem;
	/* -webkit-transform: translate(-50%, -50%); */
		transform: translate(-50%, -50%);
	}

	#nav-toggle.active{
		position: absolute;
		animation:rise 0.3s ease-in-out;
		top: 11%;
	}
	#nav-toggle{
		animation:drop 1s ease-in-out;
		top: 40%;
		left: 5%;
		display: block;
	}
    #nav.active{
        transition: top .5s ease-in-out;
        top: .1rem;
    }
	#nav{

        transition: top .5s ease-in-out;
        top: -5.5rem;
    }
    

	ul#navbar{
		margin-top: 125px;
		padding-left: 0;
	}
	ul#navbar li{
		display: block;
	}
	ul#navbar li a{
		text-align: center;
	}

}
@media (min-width: 768px) and (max-width: 992px){
	.navMenu {
		display: flex;
		min-height: 0rem;
		position: absolute;
		width: 150px;
		top: 1.7rem;
		left: 21.5rem;
	/* -webkit-transform: translate(-50%, -50%); */
		transform: translate(-50%, -50%);
	}

	#nav-toggle.active{
		position: absolute;
		animation:rise 0.3s ease-in-out;
		top: 11%;
	}
	#nav-toggle{
		animation:drop 1s ease-in-out;
		top: 40%;
		left: 5%;
		display: block;
	}
    #nav.active{
        transition: top .5s ease-in-out;
        top: .1rem;
    }
	#nav{

        transition: top .5s ease-in-out;
        top: -5.5rem;
    }
    

	ul#navbar{
		margin-top: 125px;
		padding-left: 0;
	}
	ul#navbar li{
		display: block;
	}
	ul#navbar li a{
		text-align: center;
	}
}
@media (min-width: 992px){
	#nav-toggle{
		left: 0;
		display: block;
		border-radius: 0;
	}
	#nav{
		display: none;
	}	
	ul#navbar{
		margin-left: 16px;
		animation: slide 0.3s ease;
	}
	ul#navbar li{
		margin-top: 10px;
	}
}

@keyframes drop{
	from{
		top: 10%;
	}
	to{
		top: 40%;
	}
}
@keyframes rise{
	from{
		top: 40%;
	}
	to{
		top: 11%;
	}
}
@keyframes slide{
	from{
		margin-left: -500px;
	}
	to{
		margin-left: 16px;
	}
}

</style>