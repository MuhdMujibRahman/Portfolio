<script setup>
    import image from '@/assets/image/memoji.png'
    import image2 from '@/assets/image/memoji2.png'
    import coffeMaker from '@/assets/image/coffee-maker.png'
</script>
    
    <template>
      <div class="box">
        <div id="intro">
            <div class="intro-container">
            <p>Coming Soon !</p>
            <h1 id="title"> Something's brewing</h1>
            <img id="icon" :src="coffeMaker" />
            </div>
        </div>
        <div class="wrapper">
          <div id="logo" content="width=device-width, initial-scale=1.0">
            <img
            @mouseover="hover = false"
            @mouseleave="hover = true"
            v-show="!hover" 
            :src="image" />
            <img
            @mouseover="hover = true"
            @mouseleave="hover = false"
            v-show="hover"
             :src="image2" />
          </div>
          <div class="typing-demo">
            I have python for breakfast
          </div>
        </div>

      </div>
    </template>
    
    <script>
    export default {
      data (){
        return {
          image: image,
          coffeMaker: coffeMaker,
          image2: image2,
          hover:false,
        }
      }
    }
    </script>
    
    <style scoped>

.wrapper {
  height: 45vh;
  left:-1rem;
  /*This part is important for centering*/
  display: grid;
  place-items: center;
}



@keyframes typing {
  from {
    width: 0
  }
}
    
@keyframes blink {
  50% {
    border-color: transparent
  }
}
.typing-demo {
      left: 3rem;
      grid-column: 2;
      width: 27ch;
      animation: typing 2s steps(20), blink .5s step-end infinite alternate;
      white-space: nowrap;
      overflow: hidden;
      border-right: 3px solid;
      font-family: monospace;
      font-size: 1.5rem;
      color: #385170;
}
    .box {
      margin-top: -3rem;
      display: block;
      position: relative;
      grid-template-columns: auto auto auto;
      width: 70rem;
      height: 20rem;
      border-left-width: 100rem;
      left:20rem;
      gap: 20px;
    }
    
    .box > div {
      /* background-color: rgba(255, 255, 255, 0.8); */
      padding: 20px 0;
      font-size: 30px;
      margin-top: 1rem;
    }
    
    div #logo {
      /* right: 47rem; */
      left: 15rem;
      width: 250px;
      height: 250px;
      }
    
    div > #intro {
      /* margin-right: 35rem; */
      left: 17rem;
      width: 50rem;
      height: 10rem;
      background: #e3e3e3;
      border-radius: 25px;
      box-shadow: 10px 10px #142d4c;
      text-align: center;
      margin-top: 5rem;
    }
    
    p {
      left:4rem;
      color: #142d4c;
      font-family: 'Roboto', 'Helvetica';
    }
    
    h1 {
      left:1rem;
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
      display: grid;
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

@media only screen and (min-width: 992px) and (max-width: 1200px){
      .box {
        margin-top: .5rem;
        display: gird;
        position: relative;
        grid-template-columns: auto auto auto;
        width: 60rem;
        height: 20rem;
        border-left-width: 100rem;
        left:-7.5rem;
        gap: 20px;
    }

    .wrapper {
      height: 45vh;
      left:6rem;
      /*This part is important for centering*/
      display: grid;
      place-items: center;
    }

    div#logo {
      /* right: 47rem; */
      width: 150px;
      height: 150px;
      }

      div#intro {
      /* margin-right: 35rem; */
      left: 42%;
      grid-row-start: 1;
      grid-column: 3;
      width:40rem;
      height: 8.5rem;
      background: #e3e3e3;
      border-radius: 25px;
      box-shadow: 10px 10px #142d4c;
      text-align: center;
      margin-top: 2rem;
    }

    p {
      left:4rem;
      color: #142d4c;
      font-family: 'Roboto', 'Helvetica';
    }
    
    h1 {
      font-size: 3rem;
    }



    #icon {
      margin-top: -0.5rem;
      left:0.5rem;
      width: 60px;
      height: 60px;
      grid-row: 3;
    }

    }


  
    </style>
    