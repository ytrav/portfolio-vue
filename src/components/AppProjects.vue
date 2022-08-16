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
// import AppProjectCard from "./AppProjectCard.vue";
export default {
  name: "AppProjects",
  //   components: {
  //     AppProjectCard,
  data() {
    return {
      privateProjects: [
        {
          name: "Tic-Tac-Toe",
          year: "2022",
          img: "../assets/school61.jpg",
          alt: "School 61",
        },
        {
          name: "Not Neural News",
          year: "2021",
          img: "../assets/portrait.png",
          alt: "Not Neural News",
        },
        {
          name: "DS_Store",
          year: "2021",
          img: "../assets/portrait.png",
          alt: "DS_Store",
        },
        {
          name: "Personal Portfolio",
          year: "2022",
          img: "../assets/portrait.png",
          alt: "Personal Portfolio",
        },
        {
          name: "Password Guessing Quest",
          year: "2022",
          img: "../assets/portrait.png",
          alt: "Password Guessing Quest",
        },
      ],
      workProjects: [
        {
          name: "Patient Info System",
          year: "2022",
          img: "../assets/portrait.png",
          alt: "Patient Info System",
        },
        {
          name: "MHH Dashboard",
          year: "2022",
          img: "../assets/portrait.png",
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
}
h1,
h2 {
  color: $primary;
}

h2 {
  margin: 100px 0 20px 0;
}
p {
  text-align: justify;
  color: $primary;
}

.projects {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.card {
  display: flex;
  background-color: $primary;
  color: $bg1;
  border-radius: 10px;
  flex-direction: column;
  justify-content: space-between;
  //   width: 200px;
  //   height: 150px;
  flex-grow: 1;
}
</style>