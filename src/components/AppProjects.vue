<template>
  <div id="projects" tabindex="0" @keydown.esc="popup = false">
    <h1>Projects</h1>
    <h2>Personal Projects</h2>
    <div class="projects">
      <div class="card" @click="openPopup(project)" v-for="project in privateProjects" :key="project">
        <div class="primg"><img :src="project.img" :alt="project.alt" /></div>
        <div class="prinfo">
          <h3>{{  project.name  }}</h3>
          <span>{{  project.year  }}</span>
        </div>
      </div>
    </div>
    <h2>Work Projects</h2>
    <Transition name="fade">
      <div id="popupbg" v-if="popup" @click="popup = false"></div>
    </Transition>
    <Transition name="pop">
      <div v-if="popup" class="popup">
        <img :src="project.img" :alt="project.alt" />
        <div class="popupinfo">
          <div @click="popup = false" class="close">Esc
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
              <path
                d="M19,6.41L17.59,5L12,10.59L6.41,5L5,6.41L10.59,12L5,17.59L6.41,19L12,13.41L17.59,19L19,17.59L13.41,12L19,6.41Z" />
            </svg>
          </div>
          <h1>{{  project.name  }}</h1>
          <h3>{{  project.year  }}</h3>
          <p>{{  project.desc  }}</p>
          <div :class="project.status" id="pop-cta">
            <a class="primary-button" :href="project.tryLink" target="_blank">Try it</a>
            <a class="secondary-button" :href="project.codeLink" target="_blank">See code on GitHub</a>
          </div>
        </div>
      </div>
    </Transition>

    <div class="projects">
      <div class="card" @click="openPopup(project)" v-for="project in workProjects" :key="project">
        <div class="primg"><img :src="project.img" :alt="project.alt" /></div>
        <div class="prinfo">
          <h3>{{  project.name  }}</h3>
          <span>{{  project.year  }}</span>
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
          tryLink: "https://ytrav.github.io/quest2",
          codeLink: "https://github.com/ytrav/quest2",
          status: "private",
        },
        {
          name: "Not Neural News",
          year: "Aug 2021",
          img: require("../assets/notneuralnews.png"),
          alt: "Not Neural News",
          desc: "A website that generateds random news articles from a lot of headline pieces. The website is built with vanilla HTML, CSS and JS.",
          tryLink: "https://ytrav.github.io/notneuralnews",
          codeLink: "https://github.com/ytrav/notneuralnews",
          status: "private",
        },
        {
          name: "DS_Store",
          year: "Sep 2021",
          img: require("../assets/ds_store.png"),
          alt: "DS_Store",
          desc: "An online shopping website that allows users to buy items. Or at least emulates such expierence. The website is built with vanilla HTML, CSS and JS.",
          tryLink: "https://ytrav.github.io/ds_store",
          codeLink: "https://github.com/ytrav/ds_store",
          status: "private",
        },
        {
          name: "Personal Portfolio",
          year: "Aug 2022",
          img: require("../assets/personalportfolio.png"),
          alt: "Personal Portfolio",
          desc: "This is my personal portfolio website. It is built with Vue.js and Sass. You're browsing it right now.",
          tryLink: "https://ytrav.github.io/portfolio-vue",
          codeLink: "https://github.com/ytrav/portfolio-vue",
          status: "private",
        },
        {
          name: "Password Guessing Quest",
          year: "May 2022",
          img: require("../assets/passwordguessingquest.png"),
          alt: "Password Guessing Quest",
          desc: "A simple guessing game that allows the user to guess a password to log into a fictional bake account. The website is built with vanilla HTML, CSS and JS.",
          tryLink: "https://ytrav.github.io/quest",
          codeLink: "https://github.com/ytrav/quest",
          status: "private",
        },
      ],
      workProjects: [
        {
          name: "Patient Info System",
          year: "Sep 2022",
          img: require("../assets/patientinfosystem.png"),
          alt: "Patient Info System",
          desc: "A patient information system that allows doctors to input patient details and view patient information. It was developed as an alternative to the SAP data management software. The website is built with Vue.js, HTML, and CSS. Try and code links are not available for work projects.",
          status: "work",
        },
        {
          name: "MHH Dashboard",
          year: "Sep 2022",
          // img: require("../assets/mhhdashboard.png"),
          alt: "MHH Dashboard",
          desc: "A dashboard that allows doctors to view and manage patients around the hospital, manage rooms and quickly see their symptoms, status and importance. The website is built with Vue.js, HTML, and CSS. Try and code links are not available for work projects.",
          status: "work",
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
  top: 10vh;
  left: 10vw;
  right: 10vw;
  bottom: 10vh;
  background-color: $primary;
  color: $bg1;
  z-index: 13;
  border-radius: 15px;
  overflow: auto;
  padding: 20px;
  display: flex;
  justify-content: space-between;
  gap: 50px;
  align-content: stretch;

  img {
    // zoom: 30%;
    object-fit: cover;
    // width: 100%;
    // max-width: 500px;
    max-width: 70%;
    max-height: 100%;
    border-radius: 10px 10px 0 0;
    flex-grow: 0;
    flex-shrink: 2;
    border-radius: 15px;
  }

  .popupinfo {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    flex-grow: 1;

    #pop-cta.work {
      display: none;
    }

    #pop-cta {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      justify-self: flex-end;

      a {
        text-decoration: none;
        margin-top: 15px;
        text-align: center;
        align-self: center;
        border-radius: 5000px;
        width: 200px;
        padding: 5px 20px 5px 20px;
        transition: background-color 0.1s ease-out;
      }
    }

    h1 {
      line-height: 35px;
      margin-right: 30px;
    }

    p {
      max-width: 300px;
      text-align: justify;
    }

    .primary-button {
      color: $primary;
      background-color: $bg1;

      // border: 2px solid $bg1;
      &:hover {
        background-color: #d4e4e6;
      }

      &:active {
        background-color: #abb8b9;
      }
    }

    .secondary-button {
      color: $bg1;
      border: 2px solid $bg1;

      &:hover {
        background-color: #004483;
      }

      &:active {
        background-color: #004c94;
      }
    }
  }

  /* ===== Scrollbar CSS ===== */
  /* Firefox */
  scrollbar-width: thin;
  scrollbar-color: #efffff $primary;

  /* Chrome, Edge, and Safari */
  &::-webkit-scrollbar {
    width: 10px;
  }

  &::-webkit-scrollbar-track {
    background: $primary;
    border-radius: 12px;
  }

  &::-webkit-scrollbar-thumb {
    background-color: $bg1;
    border-radius: 10px;
    border: 2px none #ffffff;

    &:hover {
      background-color: #c6d9db;
    }
  }
}

.close {
  fill: $bg1;
  cursor: pointer;
  position: absolute;
  border-radius: 5000px;
  backdrop-filter: blur(5px);
  top: 20px;
  right: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  svg {
    margin-top: -5px;
    width: 30px;
    height: 30px;
  }

  &:hover {
    svg {
      fill: #c6d9db;
    }

    color: #c6d9db;
  }

  &:active {
    svg {
      fill: #abb8b9;
    }
  }
}

@media only screen and (max-width: 1148px) and (orientation: portrait) {
  .popup {
    flex-direction: column;
    flex-wrap: nowrap;
    align-content: center;
    justify-content: center;
    padding: 60px 20px 20px 20px;

    img {
      max-width: 100%;
      margin-top: 50px;
    }

    .popupinfo {
      align-items: stretch;

      p {
        max-width: 100%;
      }

      .primary-button,
      .secondary-button {
        align-self: flex-start;
        width: 100% !important;
      }
    }
  }
}

@media only screen and (max-width: 1111px) and (orientation: landscape) {
  .popup {
    img {
      max-width: 60%;
    }
  }
}

@media only screen and (max-width: 540px) {
  .popup {
    .popupinfo {

      .primary-button,
      .secondary-button {
        width: 100% !important;
      }

      #pop-cta {
        a {
          width: 100% !important;
        }
      }
    }
  }
}

@media only screen and (max-width: 400px),
(max-height: 411px) {
  .popup {
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    border-radius: 0;

    .close {
      position: fixed;
      top: 15px;
      right: 15px;
    }
  }
}

@media only screen and (max-width: 831px) and (orientation: landscape) {
  .popup {
    .popupinfo {

      .primary-button,
      .secondary-button {
        max-width: 160px;
      }
    }
  }
}

// // remove #projects padding when viewport width is less than 360px

// @media only screen and (max-width: 360px) {
//   #projects {
//     padding: 0;
//   }
// }
</style>