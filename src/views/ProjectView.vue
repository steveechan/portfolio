<template>
  <div class="container">
    <div class="title"> 1 </div>
    <div class="title"> 2 </div>
    <div class="title"> 3 </div>
    <div class="title"> 4 </div>
  </div>
  <div class="container">
    <div class="box"> 1 </div>
    <div class="box"> 2 </div>
    <div class="box"> 3 </div>
    <div class="box"> 4 </div>
  </div>
</template>

<style>

.container {
  width: 100%;
  height: auto;
  display: flex;
  flex-direction: row;
  justify-content: space-around; 
  flex-flow: wrap;
}

.box {
  width: 300px;
  height: 300px;
  background: yellow;
  margin: 20px;
  box-sizing: border-box;
  font-size: 50px;
}
</style>
