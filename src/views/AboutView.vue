<template>
  <div class="about">
    <div class="school">
      <h1 class="who"> Who am I? </h1>
      <h1 class="whoinfo"> I am a senior at New Jersey Institute of Technology. I have a strong passion for front-end development and it has become a passion of mine. </h1>
    </div>
    <div class="bio">
      Hello
    </div>
    <div class="skills">
      <h1 v-if="isHidden" class="skillsInfo"> Languages/Frameworks </h1>
      <h1 class="skill"> {{ languages[count] }}</h1> 
      <button v-if="isHidden" @click="showSkills();isHidden = !isHidden"> Show More </button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isHidden: true,
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
        this.count = this.count + 1
      }, 1000);
    }
  }
}
</script>

<style>

.skill {
  text-align: center;
}
.about {
  width: 100vh;
}
.school {
  width: 400px;
  height: 400px;
}
.who {
  font-family: monospace;
}

.whoinfo {
  font-size: 25px;
}

.skills {
  position: absolute;
  left: 45%;
  top: 10%;
  text-align: center;
}

.skillsInfo {
    font-family: monospace;
}
</style>
