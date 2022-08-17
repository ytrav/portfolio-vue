<template>
  <div id="projects">
    <h1>Projects</h1>
    <h2>Personal Projects</h2>
    <div class="projects">
      <div
        class="card"
        @click="openPopup(project)"
        v-for="project in privateProjects"
        :key="project"
      >
        <div class="primg"><img :src="project.img" :alt="project.alt" /></div>
        <div class="prinfo">
          <h3>{{ project.name }}</h3>
          <span>{{ project.year }}</span>
        </div>
      </div>
    </div>
    <h2>Work Projects</h2>
    <Transition name="fade">
      <div id="popupbg" v-if="popup" @click="popup = false"></div>
    </Transition>
    <Transition name="pop">
      <div v-if="popup" class="popup">
      <div @click="popup=false" class="close">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M19,6.41L17.59,5L12,10.59L6.41,5L5,6.41L10.59,12L5,17.59L6.41,19L12,13.41L17.59,19L19,17.59L13.41,12L19,6.41Z" /></svg>
      </div>
        <img :src="project.img" :alt="project.alt" />
        <div class="popupinfo">
          <h3>{{ project.name }}</h3>
          <span>{{ project.year }}</span>
          <p>{{ project.desc }}</p>
        </div>
      </div>
    </Transition>

    <div class="projects">
      <div
        class="card"
        @click="openPopup(project)"
        v-for="project in workProjects"
        :key="project"
      >
        <div class="primg"><img :src="project.img" :alt="project.alt" /></div>
        <div class="prinfo">
          <h3>{{ project.name }}</h3>
          <span>{{ project.year }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppProjects",
  methods: {
    getImagePath: function (project) {
      return project.img;
    },
    openPopup: function (project) {
      this.project = project;
      this.popup = true;
    },
  },
  data() {
    return {
      popup: false,
      project: "",
      privateProjects: [
        {
          name: "Tic-Tac-Toe",
          year: "May 2022",
          img: require("../assets/tictactoe.png"),
          alt: "Tic-Tac-Toe",
          desc: "A simple tic-tac-toe game built with vanilla HTML, CSS and JS. Allows for two players to play against each other. Doesn't feature any AI yet.",
        },
        {
          name: "Not Neural News",
          year: "Aug 2021",
          img: require("../assets/notneuralnews.png"),
          alt: "Not Neural News",
          desc: "A website that generateds random news articles from a lot of headline pieces. The website is built with vanilla HTML, CSS and JS.",
        },
        {
          name: "DS_Store",
          year: "Sep 2021",
          img: require("../assets/ds_store.png"),
          alt: "DS_Store",
          desc: "An online shopping website that allows users to buy items. Or at least emulates such expierence. The website is built with vanilla HTML, CSS and JS.",
        },
        {
          name: "Personal Portfolio",
          year: "Aug 2022",
          img: require("../assets/personalportfolio.png"),
          alt: "Personal Portfolio",
          desc: "This is my personal portfolio website. It is built with Vue.js and Sass. You're browsing it right now.",
        },
        {
          name: "Password Guessing Quest",
          year: "May 2022",
          img: require("../assets/passwordguessingquest.png"),
          alt: "Password Guessing Quest",
          desc: "A simple guessing game that allows the user to guess a password to log into a fictional bake account. The website is built with vanilla HTML, CSS and JS.",
        },
      ],
      workProjects: [
        {
          name: "Patient Info System",
          year: "Sep 2022",
          // img: require("../assets/patientinfosystem.png"),
          alt: "Patient Info System",
        },
        {
          name: "MHH Dashboard",
          year: "Sep 2022",
          // img: require("../assets/mhhdashboard.png"),
          alt: "MHH Dashboard",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
$primary: #00315f;
$bg1: #efffff;
$bg2: #e3f5f7;

#projects {
  padding: 60px;
  margin-top: 5px;
  background-color: $primary;
}
h1,
h2 {
  color: $bg1;
}

h2 {
  margin: 100px 0 20px 0;
}
p {
  text-align: justify;
  color: $bg1;
}

.projects {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.card {
  display: flex;
  background-image: linear-gradient(to left, $bg1, $bg2);
  color: $primary;
  border-radius: 10px;
  // max-width: 400px;
  max-height: 300px;
  min-width: 200px;
  max-width: 300px;
  flex-direction: column;
  //   width: 200px;
  //   height: 150px;
  flex-grow: 1;
  flex-shrink: 1;
  flex: 1;
  transition: transform 0.1s ease-out;
  cursor: pointer;
  &:hover {
    transform: scale(1.1);
  }
  img {
    // zoom: 30%;
    object-fit: fit;
    width: 100%;
    border-radius: 10px 10px 0 0;
  }
  .prinfo {
    margin: 10px;
    h3 {
      font-size: 1.4em;
    }
    span {
      font-size: 1.1em;
    }
  }
}

// popup styling

#popupbg {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 12;
}

.popup {
  position: fixed;
  top: 5vh;
  left: 5vw;
  right: 5vw;
  bottom: 5vh;
  background-color: $primary;
  color: $bg1;
  z-index: 13;
  border-radius: 10px;
  padding: 20px;
  img {
    // zoom: 30%;
    object-fit: fit;
    width: 100%;
    border-radius: 10px 10px 0 0;
  }
}

.close {
  fill: $bg1;
  cursor: pointer;
  width: 30px;
  height: 30px;
}

</style>