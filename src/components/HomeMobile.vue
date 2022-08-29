<script setup>
    import image from '@/assets/image/memoji.png'
    import coffeMaker from '@/assets/image/coffee-maker.png'
    </script>
    
    <template>
      <div class="box">
          <div id="logo" content="width=device-width, initial-scale=1.0">
            <img :src="image" />
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
      data (){
        return {
          image: image,
          coffeMaker: coffeMaker,
        }
      }
    }
    </script>
    
<style scoped>
    
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
      box-shadow: 10px 10px #142d4c;
    
    }
    
    .box > div {
      /* background-color: rgba(255, 255, 255, 0.8); */
      padding: 20px 0;
      font-size: 30px;
      margin-top: 1rem;
    }
    
    div #logo {
      grid-row-start: 1;
      grid-column-end: 3;
      /* right: 47rem; */
      left: 37rem;
      width: 150px;
      height: 150px;
      }
    
    div > #intro {

      /* margin-right: 35rem; */
      left: 34rem;
      grid-row-start: 2;
      grid-column-end: 3;
      width: 15rem;
      height: 15rem;
      background: #e3e3e3;
      border-radius: 25px;
      box-shadow: 10px 10px;
      text-align: center;
      /* margin-top: 5rem; */
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
</style>
    