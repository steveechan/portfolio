<template>
  <div class="home">
    <div class="intro">
      <h1 class="hey"> Hey I'm </h1>
      <h1 class="name"> Stephen Chan! </h1> <img src="../assets/AvatarMaker.png">
      <router-link to="/project"><button class="contact">Contact Me</button></router-link>
      <h1 class="info"> Welcome to my world. </h1>
    </div>
    <div class="buttons">
    <a href="https://www.linkedin.com/in/stephen---chan/"><button class="linkedin">
      <h1> LinkedIn </h1>
    </button>
    </a>
    <a href="https://github.com/steveechan"><button class="github">
      <h1> GitHub </h1>
    </button>
    </a>
    </div>
    
  </div>
</template>

<script>

</script>


<style scoped>

.contact:hover {
  font-size: 10px;
}
img {
  width: 200px;
  height: 200px;
  object-fit: cover;
  border-radius: 50%;
}
.buttons {
  position: relative;
  left: 110px;
  top: -320px;
  width: 100vh;
}

.linkedin:hover {
  font-size: 10px;
}

.github:hover {
  font-size: 10px;
}

.info {
  font-size: 50px;
  font-weight: bold;
  font-family: monospace;
  letter-spacing: 7px;
  text-transform: uppercase;
  background: linear-gradient(to right, 
  hsl(261, 98%, 48%) 0, 
  hsl(187, 97%, 36%) 10%, 
  hsl(0, 0%, 100%) 20%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: shine 2s infinite linear;
  padding: 120px;
  
}
.hey {
  font-size: 30px;
  font-weight: bold;
  font-family: monospace;
  letter-spacing: 7px;
  cursor: pointer;
  text-transform: uppercase;
  background: linear-gradient(to right, 
  hsl(261, 98%, 48%) 0, 
  hsl(187, 97%, 36%) 10%, 
  hsl(0, 0%, 100%) 20%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: shine 4s infinite linear;
}

@keyframes shine {
  0% {
    background-position: 0;
  }
  60% {
    background-position: 600px;
  }
  100% {
  background-position: 600px;
  }
}

.intro {
text-align: left;
margin: 30px;
padding: 0px;
position: relative;
}

.name {
  width: 100vh;
  position: relative;
  left: 40px;
  font-size: 50px;
  font-weight: bold;
  font-family: monospace;
  letter-spacing: 7px;
  cursor: pointer;
  text-transform: uppercase;
  background: linear-gradient(to right, 
  hsl(273, 98%, 48%) 0, 
  hsl(347, 90%, 48%) 10%, 
  hsl(0, 0%, 100%) 20%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: nameshine 4s infinite linear;
}

@keyframes nameshine {
  0% {
    background-position: 0;
  }
  60% {
    background-position: 600px;
  }
  100% {
  background-position: 600px;
  }
}
</style>
