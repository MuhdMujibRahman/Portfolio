<template>
<div class="frame">
  <button class="custom-btn btn-3"><span>Download CV</span></button>
  <button class="custom-btn btn-4"><span>Hire Me</span></button>
</div>


</template>


<style scoped>
.frame {
  width: 50vh;
  /* margin: 40px auto; */
  text-align: center;
  display: grid;
  font-family: 'Roboto', sans-serif;
}
button {
  margin: 10px;
}
.custom-btn {
  width: 130px;
  height: 40px;
  color: #fff;
  border-radius: 5px;
  padding: 10px 25px;
  font-family: 'Lato', sans-serif;
  font-weight: 500;
  background: transparent;
  cursor: pointer;
  transition: all 0.3s ease;
  position: relative;
  display: inline-block;
   
  outline: none;
}



/* 3 */
.btn-3 {
  grid-row-start:1;
  background: rgb(0,172,238);
  background: linear-gradient(0deg, rgba(0,172,238,1) 0%, rgba(2,126,251,1) 100%);
  width: 200px;
  height: 60px;
  line-height: 60px;
  padding: 0;
  border: none;
  box-shadow:inset 2px 2px 2px 0px rgba(255,255,255,.5),
   7px 7px 20px 0px rgba(0,0,0,.1),
   4px 4px 5px 0px rgba(0,0,0,.1);
   font-size: 20px;
  
}
.btn-3 span {
  position: relative;
  display: block;
  width: 100%;
  height: 100%;
}
.btn-3:before,
.btn-3:after {
  position: absolute;
  content: "";
  right: 0;
  top: 0;
   background: rgba(2,126,251,1);
  transition: all 0.3s ease;
}
.btn-3:before {
  height: 0%;
  width: 2px;
}
.btn-3:after {
  width: 0%;
  height: 2px;
}
.btn-3:hover{
   background: transparent;
  box-shadow: none;
}
.btn-3:hover:before {
  height: 100%;
}
.btn-3:hover:after {
  width: 100%;
}
.btn-3 span:hover{
   color: rgba(2,126,251,1);
}
.btn-3 span:before,
.btn-3 span:after {
  position: absolute;
  content: "";
  left: 0;
  bottom: 0;
   background: rgba(2,126,251,1);
  transition: all 0.3s ease;
}
.btn-3 span:before {
  width: 2px;
  height: 0%;
}
.btn-3 span:after {
  width: 0%;
  height: 2px;
}
.btn-3 span:hover:before {
  height: 100%;
}
.btn-3 span:hover:after {
  width: 100%;
}

/* btn 4 */
.btn-4{
  grid-row-start:1;
  /* background: rgb(0,172,238); */
  /* background: linear-gradient(0deg, rgba(0,172,238,1) 0%, rgba(2,126,251,1) 100%); */
  width: 200px;
  height: 60px;
  line-height: 60px;
  padding: 0;
  border: none;
  font-size: 20px;
  
}
.btn-4 span {
  color: #005792;
  position: relative;
  display: block;
  width: 100%;
  height: 100%;
}
.btn-4:before,
.btn-4:after {
  position: absolute;
  content: "";
  right: 0;
  top: 0;
   background: rgba(2,126,251,1);
  transition: all 0.3s ease;
}
.btn-4:before {
  height: 100%;
  width: 2px;
}
.btn-4:after {
  width: 100%;
  height: 2px;
}
.btn-4:hover{
   background: transparent;
  box-shadow: none;
}
.btn-4:hover:before {
  height: 0%;
}
.btn-4:hover:after {
  width: 0%;
}
.btn-4 span:hover{
   color: rgba(2,126,251,1);
}
.btn-4 span:before,
.btn-4 span:after {
  position: absolute;
  content: "";
  left: 0;
  bottom: 0;
   background: rgba(2,126,251,1);
  transition: all 0.3s ease;
}
.btn-4 span:before {
  width: 1px;
  height: 100%;
}
.btn-4 span:after {
  width: 100%;
  height: 1px;
}
.btn-4 span:hover:before {
  height: 0%;
}
.btn-4 span:hover:after {
  width: 0%;
}
</style>