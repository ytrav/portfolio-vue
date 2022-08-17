<template>
  <div id="projects">
    <h1>Projects</h1>
    <h2>Personal Projects</h2>
    <div class="projects">
      <div class="card" v-for="project in privateProjects" :key="project">
        <div class="primg"><img :src="project.img" :alt="project.alt" /></div>
        <div class="prinfo">
          <h3>{{ project.name }}</h3>
          <span>{{ project.year }}</span>
        </div>
      </div>
    </div>
    <h2>Work Projects</h2>
    <div class="projects">
      <div class="card" v-for="project in workProjects" :key="project">
        <div class="primg"><img :src="getImagePath(project)" :alt="project.alt" /></div>
        <div class="prinfo">
          <h3>{{ project.name }}</h3>
          <span>{{ project.year }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import AppProjectCard from "./AppProjectCard.vue";
export default {
  name: "AppProjects",
  //   components: {
  //     AppProjectCard,
  methods: {
    // method that gets dynamic image path from project object
    getImagePath: function(project) {
      return "img/projects/" + project.img;
    },
  },
  data() {
    return {
      privateProjects: [
        {
          name: "Tic-Tac-Toe",
          year: "May 2022",
          img: require("../assets/tictactoe.png"),
          alt: "Tic-Tac-Toe",
        },
        {
          name: "Not Neural News",
          year: "Aug 2021",
          img: require("../assets/notneuralnews.png"),
          alt: "Not Neural News",
        },
        {
          name: "DS_Store",
          year: "Sep 2021",
          img: require("../assets/ds_store.png"),
          alt: "DS_Store",
        },
        // {
        //   name: "Personal Portfolio",
        //   year: "Aug 2022",
        //   img: require("../assets/personalportfolio.png"),
        //   alt: "Personal Portfolio",
        // },
        // {
        //   name: "Password Guessing Quest",
        //   year: "May 2022",
        //   img: require("../assets/passwordguessingquest.png"),
        //   alt: "Password Guessing Quest",
        // },
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
</style>