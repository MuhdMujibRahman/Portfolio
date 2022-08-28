<script setup>
import image from '@/assets/memoji.png'
import coffeMaker from '@/assets/coffee-maker.png'
</script>

<template>
  <div class="box">
      <div id="logo">
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
  display: grid;
  position: relative;
  grid-template-columns: auto auto auto;
  width: 70rem;
  height: 20rem;
  border-left-width: 100rem;
  left:5rem;
  gap: 20px;

}

.box > div {
  /* background-color: rgba(255, 255, 255, 0.8); */
  padding: 20px 0;
  font-size: 30px;
  margin-top: 1rem;
}

div #logo {
  grid-row-start: 1;
  grid-column-end: 2;
  margin-left: 10rem;
  width: 250px;
  height: 250px;
}

div #intro {
  margin-right: 35rem;
  grid-row-start: 1;
  width: 50rem;
  height: 10rem;
  background: #e3e3e3;
  border-radius: 25px;
  box-shadow: 10px 10px;
  text-align: center;
  margin-top: 5rem;
}

p {
  color: #142d4c;
  font-family: 'Roboto', 'Helvetica';
}

h1 {
  color: #142d4c;
  font-family: 'Roboto', 'Helvetica';
  font-weight: 999;
}

img {
  height: inherit;
  width: inherit;
}

.intro-container {
  display: grid;
}

#icon {
  margin-top: 15px;
  width: 60px;
  height: 60px;
  grid-row: 3;
}

#title {
  grid-row: 3
}

</style>
