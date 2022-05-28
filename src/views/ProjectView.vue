<template>
  <div class="container">
	<div class="box"> Crypto Portfolio<img src="../assets/btc.png"> <button v-if="buttonhover"> View </button></div>
	<div class="box2"> Salary Expense Tracker<img src="../assets/dollar.png"> </div>
	<div class="box"> Fullstack Pong<img src="../assets/pong.png"> </div>
	<div class="box2"> Weather App </div>
	<div class="box"> Movie Search </div>
</div>
</template>

<script>
export default {
	data() {
		buttonhover = true;
	}
}
</script>

<style>

img {
	max-width: 100%;
}
.container {
	width: 90%;
	padding: 20px;
	margin: 100px auto;
	display: flex;
	flex-direction: row;
	justify-content: center;
}

.box2,
.box {
width: 250px;
height: 280px;
background: #05cee9;
	margin: 0px 10px;
  	transition: 1s;
  	font-weight: bold;
  	color: black;
	text-align: center;
	font-size: 13px;
	font-family: monospace;
	font-size: 20px;
}
.box:hover {
	transform: scale(1.3);
	background: rgba(2, 151, 177, 0.521);
	z-index: 2;
  	letter-spacing: 3px;
	box-shadow: 2px 2px 2px #000;
}

.box2:hover {
  	transform: rotate(360deg);
  	background: rgba(2, 151, 177, 0.521);
}
</style>
