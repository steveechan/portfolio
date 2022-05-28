<template>
  <div class="about">
    <div class="school">
      <h1 data-text="Who?" class="who"> Who? </h1>
      <h1 class="whoinfo"> I am a senior at New Jersey Institute of Technology. I am a self taught and determined front-end developer. My main front-end framework is Vue.js 
        and my most proficient languages are Java and JavaScript. I love developing new web applications and solving coding problems. </h1>
    </div>
    <div class="bio">
      <h1 data-text="Why?" class="why"> Why? </h1>
      <h1 class="bioinfo">
      My interest for programming started at a young age when I played a game called ROBLOX. They had a studio mode where you could create your own games with the language "LUA".
      That interest had sparked within me when I took a class called Internet Applications where we created our own fullstack application.  </h1>
    </div>
    <div class="skills">
      <h1 data-text="Languages/Frameworks" class="skillsInfo"> Languages/Frameworks </h1>
      <h1 class="skill"> {{ languages[count] }}</h1> 
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    this.showSkills();
  },
  data() {
    return {
      count: 0,
      languages: [
        "Java",
        "JavaScript",
        "HTML",
        "CSS",
        "C++",
        "C#",
        "Python",
        "Vue.js",
        "React.js",
        "mySQL",
        "PHP",
      ]
    };
  },
  methods: {
    showSkills: function () {
      setInterval(() => {
        this.counting()
      }, 1000);
    },

    counting: function() {
      this.count++;
      if(this.count === this.languages.length - 1) {
        this.count = 0;
      }
    }

  }
}
</script>

<style>

.why {
  color: white;
  font-size: 5vw;
  text-transform: uppercase;
  font-family: monospace;
  text-align: center;
}

.why::before {
  content: attr(data-text);
  position: absolute;
  width: 100%;
  color: #05cee9;
  -webkit-text-stroke: 0vw #383d52;
  font-family: monospace;
  text-align: center;
  overflow: hidden;
  animation: animate 6s linear infinite;
}

@keyframes animate {
  0%, 10%, 100%
  {
    width: 0;
  }
  70%, 90%
  {
    width: 11%;
  }
}

@keyframes animate2 {
  0%, 10%, 100%
  {
    width: 0;
  }
  70%, 90%
  {
    width: 100%;
  }
}

@keyframes animate3 {
  0%, 10%, 100%
  {
    width: 0;
  }
  70%, 90%
  {
    width: 4.4%;
  }
}


.skill {
  text-align: center;
}

.skillsInfo::before {
  content: attr(data-text);
  position: absolute;
  width: 100%;
  color: #05cee9;
  -webkit-text-stroke: 0vw #383d52;
  font-family: monospace;
  text-align: center;
  overflow: hidden;
  animation: animate2 6s linear infinite;
}
.skills {
  position: absolute;
  top: 10%;
  left: 50%;
  color: white;
  font-size: 2vw;
  text-transform: uppercase;
}
.bioinfo {
  font-family: monospace;
}
.about {
  width: 100vh;
}
.school {
  width: 400px;
  height: 400px;
}
.who {
  color: white;
  font-size: 2vw;
  text-transform: uppercase;
  font-family: monospace;
  text-align: center;
}

.who::before {
  content: attr(data-text);
  position: absolute;
  width: 100%;
  color: #05cee9;
  -webkit-text-stroke: 0vw #383d52;
  font-family: monospace;
  text-align: center;
  overflow: hidden;
  animation: animate3 6s linear infinite;
}

.whoinfo {
  font-size: 25px;
  font-family: monospace;
}

.skillsInfo {
    font-family: monospace;
}
</style>
