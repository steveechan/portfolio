<template>
  <div class="container">
	<div class="box"
		@mouseover="buttonhover = true" 
		@mouseleave="buttonhover = false"> 
		Crypto Portfolio
		<img src="../assets/btc.png"> 
		<a v-bind:href="crypto">
		<button v-if="buttonhover"> View </button>
		</a>
	</div>
	<div class="box2"
		@mouseover="buttonhover2 = true" 
		@mouseleave="buttonhover2 = false"> 
		Salary Expense Tracker
		<img src="../assets/dollar.png">
		<a v-bind:href="salary">
		<button v-if="buttonhover2"> View </button>
		</a>
	</div>
	<div class="box"
		@mouseover="buttonhover3 = true" 
		@mouseleave="buttonhover3 = false"> 
		Fullstack Pong
		<img src="../assets/pong.png"> 
		<a v-bind:href="pong"> 
		<button v-if="buttonhover3"> View </button>
		</a>
	</div>
	<div class="box2"
		@mouseover="buttonhover4 = true" 
		@mouseleave="buttonhover4 = false"> 
		Weather App
		<img src="../assets/weather.png">
		<a v-bind:href="weather">
		<button v-if="buttonhover4"> View </button>
		</a>
	</div>
	<div class="box"
		@mouseover="buttonhover5 = true" 
		@mouseleave="buttonhover5 = false"> 
		Movie Search
		<img src="../assets/search.png">
		<a v-bind:href="movie">
		<button v-if="buttonhover5"> View </button>
		</a>
	</div>
</div>
</template>

<script>
export default {
	data() {
		return {
			salary: "https://steveechan.github.io/tracker/salaryexpense/index.html",
			crypto: "https://vue-crypto-portfolio.netlify.app/",
			movie: "https://github.com/steveechan/movie-project",
			weather: "https://github.com/steveechan/WeatherApp",
			pong: "https://sc2347-prod.herokuapp.com/Project/login.php",
			buttonhover: false,
			buttonhover2: false,
			buttonhover3: false,
			buttonhover4: false,
			buttonhover5: false,
		}
	}
}
</script>

<style scoped>

button {
    display:inline-block;
	padding:0.7em 1.4em;
	margin:0 0.3em 0.3em 0;
	border-radius:0.15em;
	box-sizing: border-box;
	text-decoration:none;
	font-family:'Roboto',sans-serif;
	text-transform:uppercase;
	font-weight:400;
	color:#FFFFFF;
	background-color:#3369ff;
	box-shadow:inset 0 -0.6em 0 -0.35em rgba(0,0,0,0.17);
	text-align:center;
	position:relative;
}


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
	box-shadow: 0px 0px 20px rgb(5,206,233);
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
