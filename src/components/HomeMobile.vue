<script setup>
    import image from '@/assets/image/memoji.png'
    import coffeMaker from '@/assets/image/coffee-maker.png'
    </script>
    
    <template>
      <div class="box">
        <div class="wrapper" :class="{ active: navBarIsActive }">
          <div class="logo-container">
            <div id="logo" content="width=device-width, initial-scale=1.0">
            <img :src="image" />
          </div>
          </div>
          <div class="typing-demo">
            I have python for breakfast
          </div>
        </div>
          <div id="intro">
            <div class="intro-container">
            <p>Coming Soon !</p>
            <h1 id="title"> Something's brewing</h1>
            <img id="icon" :src="coffeMaker" />
            </div>
          </div>
      </div>
    </template>
    
<script>
export default {
  name: 'HomeMobile',
  props: {
      navBarIsActive: Boolean,
    },
      data (){
        return {
          image: image,
          coffeMaker: coffeMaker,
        }
      }
    }
</script>
    
<style scoped>
.typing-demo {
  color: #385170;;
}
@keyframes typing {
  from {width: 0}
}
    
@keyframes blink {
  50% {border-color: transparent}
  100% {border-color: transparent}
}
    .wrapper {
      height: 15vh;
      width: 39vh;
      left:-2rem;
      /*This part is important for centering*/
      display: grid;
      top:-3.5rem;
      place-items: center;
    }


    .logo-container { 
      grid-row-start: 1;
    }



    .box {
      margin-top: 5rem;
      display: grid;
      position: relative;
      grid-template-columns: auto auto auto;
      width: fit-content;
      height: 20rem;
      border-left-width: 100rem;
      left:-30.9rem;
      gap: 20px;
    
    }
    
    .box > div {
      /* background-color: rgba(255, 255, 255, 0.8); */
      padding: 20px 0;
      font-size: 30px;
      margin-top: 1rem;
    }
    
    div#logo {
      transition: left  .9s ease-in-out, opacity .9s;
      opacity: 10;
      grid-row-start: 1;
      grid-column-end: 3;
      /* right: 47rem; */
      left: 37rem;
      width: 150px;
      height: 150px;
      }

    
    div#intro {

      /* margin-right: 35rem; */
      left: 17.5rem;
      grid-row-start: 2;
      grid-column-end: 3;
      width: 15rem;
      height: 15rem;
      background: #e3e3e3;
      border-radius: 25px;
      box-shadow: 10px 10px #142d4c;
      text-align: center;
      margin-top: 5rem;
    }
    
    p {
        font-size: 1rem;
      left:0.5rem;
      color: #142d4c;
      font-family: 'Roboto', 'Helvetica';
    }
    
    h1 {
    
      font-size: 2rem;
      left:0.3rem;
      color: #142d4c;
      font-family: 'Roboto', 'Helvetica';
      font-weight: 999;
    }
    
    img {
      height: inherit;
      width: inherit;
    }
    
    .intro-container {
      text-align: center;
      display: block;
    }
    
    #icon {
      margin-top: 17px;
      margin-left: 15px;
      width: 60px;
      height: 60px;
      grid-row: 3;
    }
    
    #title {
      grid-row: 3
    }
@media only screen and (max-width: 360px){
  .box {
      margin-top: 5rem;
      display: grid;
      position: relative;
      grid-template-columns: auto auto auto;
      width: fit-content;
      height: 20rem;
      border-left-width: 100rem;
      left:-32.9rem;
      gap: 20px;
    
    }
  div#logo.active {
      transition: left .9s ease-in-out;
      left: 39rem;

    }
    .typing-demo {
      margin-top: 2rem;
      left: 37rem;
      grid-row-start: 2;
      width: 27ch;
      animation: typing 2s steps(20), blink .5s step-end infinite alternate;
      white-space: nowrap;
      overflow: hidden;
      border-right: 3px solid;
      font-family: monospace;
      font-size: 1rem;
   }
   .wrapper {
      transition: left .9s ease-in-out;
      left: -1rem;

    }
    .wrapper.active {
      transition: left .9s ease-in-out;
      left: 4rem;

    }
  
}

@media only screen and (max-width: 380px) and (min-width: 361px){
  .box {
      margin-top: 5rem;
      display: grid;
      position: relative;
      grid-template-columns: auto auto auto;
      width: fit-content;
      height: 20rem;
      border-left-width: 100rem;
      left:-30.7rem;
      gap: 20px;
    
    }
    /* div#logo.active {
      transition: left .9s ease-in-out;
      left: 39rem;

    } */
    .typing-demo {
      margin-top: 2rem;
      left: 37rem;
      grid-row-start: 2;
      width: 27ch;
      animation: typing 2s steps(20), blink .5s step-end infinite alternate;
      white-space: nowrap;
      overflow: hidden;
      border-right: 3px solid;
      font-family: monospace;
      font-size: 1rem;
    }
    .wrapper {
      transition: left .9s ease-in-out;
      left: -3rem;

    }
    .wrapper.active {
      transition: left .9s ease-in-out;
      left: 4rem;

    }
  
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
      left:-57vh;
      gap: 20px;
    

    }

    div#intro {

      /* margin-right: 35rem; */
      margin-left: -4.5rem;
      margin-right: 10rem;
      grid-row-start: 2;
      grid-column-end: 3;
      width: 15rem;
      height: 15rem;
      background: #e3e3e3;
      border-radius: 25px;
      box-shadow: 10px 10px #142d4c;
      text-align: center;
      margin-top: 5rem;
      }
      .wrapper {
          height: 15vh;
          width: 39vh;
          left:-3.5rem;
          /*This part is important for centering*/
          display: grid;
          top:-5rem;
          place-items: center;
    }
    .typing-demo {
      margin-top: 2rem;
      left: 37rem;
      grid-row-start: 2;
      width: 27ch;
      animation: typing 2s steps(20), blink .5s step-end infinite alternate;
      white-space: nowrap;
      overflow: hidden;
      border-right: 3px solid;
      font-family: monospace;
      font-size: 1rem;
    }
    .wrapper {
      transition: left .9s ease-in-out;
      left: -4rem;

    }
    .wrapper.active {
      transition: left .9s ease-in-out;
      left: 4rem;

    }

}

@media (min-width: 481px) and (max-width: 767px){
  .box {
      margin-top: 2rem;
      margin-bottom:2.8rem;
      display: grid;
      position: relative;
      grid-template-columns: auto auto auto;
      width: 100vh;
      height: 20rem;
      border-left-width: 100rem;
      left:-35rem;
      gap: 20px;
    

  }
  .intro-container {
      text-align: center;
      display: grid;
    }
  div#intro {

    /* margin-right: 35rem; */
      left: 36.9rem;
      grid-row-start: 1;
      grid-column:3;
      width: 25rem;
      height: 7rem;
      background: #e3e3e3;
      border-radius: 25px;
      box-shadow: 10px 10px #142d4c;
      text-align: center;
  /* margin-top: 5rem; */
  }
  #icon {
      margin-top: 10px;
      margin-left: 15px;
      width: 40px;
      height: 40px;
      grid-row: 3;
    }
        
    #title {
      grid-row: 3
    }
    div #logo {
      grid-row-start: 1;
      grid-column-end: 3;
      /* right: 47rem; */
      left: 37rem;
      width: 150px;
      height: 150px;
      top: -1.5rem;
      }
      .logo-container { 
        top:1rem;
        grid-row-start: 1;
      }
      .wrapper {
        height: 15vh;
        width: 39vh;
        left:1rem;
        /*This part is important for centering*/
        display: grid;
        top:3rem;
        place-items: center;
    }

}
@media (min-width: 768px) and (max-width: 992px){
  .box {
      margin-top: 2rem;
      margin-bottom: 5.5rem;
      display: grid;
      position: relative;
      grid-template-columns: auto auto auto;
      width: 100vh;
      height: 20rem;
      border-left-width: 100rem;
      left:-30rem;
      gap: 20px;
    

  }
  .intro-container {
      text-align: center;
      display: grid;
    }
  div > #intro {

    /* margin-right: 35rem; */
      left: 36.9rem;
      grid-row-start: 1;
      grid-column:3;
      width: 25rem;
      height: 7rem;
      background: #e3e3e3;
      border-radius: 25px;
      box-shadow: 10px 10px #142d4c;
      text-align: center;
  /* margin-top: 5rem; */
  }
  #icon {
      margin-top: 10px;
      margin-left: 15px;
      width: 40px;
      height: 40px;
      grid-row: 3;
    }
        
    #title {
      grid-row: 3
    }
    div #logo {
      grid-row-start: 1;
      grid-column-end: 3;
      /* right: 47rem; */
      left: 37rem;
      width: 150px;
      height: 150px;
      top: -1.5rem;
      }
      .wrapper {
        height: 15vh;
        width: 39vh;
        left:1rem;
        /*This part is important for centering*/
        display: grid;
        top:3rem;
        place-items: center;
    }
}

</style>
    