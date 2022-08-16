<template>
  <svg
    @click="open = !open"
    id="menu-button"
    xmlns="http://www.w3.org/2000/svg"
    viewBox="0 0 24 24"
  >
    <path d="M3,6H21V8H3V6M3,11H21V13H3V11M3,16H21V18H3V16Z" />
  </svg>
  <Transition name="fade">
    <div @click="open = false" v-if="open" id="burgerdark"></div>
  </Transition>
  <Transition name="slide">
    <NavMenu @closeMenu="closeMenu($event)" v-if="open" />
  </Transition>
  <Transition appear name="initial">
    <AppLanding />
  </Transition>
  <AppAbout />
  <AppExperience />
  <AppProjects />
</template>

<script>
import AppLanding from "./components/AppLanding.vue";
import AppAbout from "./components/AppAbout.vue";
import AppExperience from "./components/AppExperience.vue";
import NavMenu from "./components/NavMenu.vue";
import AppProjects from "./components/AppProjects.vue";

export default {
  name: "App",
  data() {
    return {
      open: false,
    };
  },
  methods: {
    closeMenu(data) {
      this.open = data;
    },
  },
  components: {
    AppLanding,
    AppAbout,
    AppExperience,
    NavMenu,
    AppProjects,
  },
};
</script>

<style lang="scss">
$primary: #00315f;
$bg1: #efffff;
$bg2: #e3f5f7;

@font-face {
  font-family: "Kanit";
  src: url("./assets/Kanit-Regular.ttf"), url("./assets/Kanit-Medium.ttf");
}

@font-face {
  font-family: "Poppins";
  src: url("./assets/Poppins-Medium.ttf");
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Kanit", Verdana, Geneva, Tahoma, sans-serif;
  scroll-behavior: smooth;
  // border: 1px solid rgba(255, 0, 0, 0.479);
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.slide-enter-active,
.slide-leave-active {
  transition: all 0.3s ease;
}


.slide-enter-from,
.slide-leave-to {
  opacity: 0;
  transform: translateX(200px);
}

#burgerdark {
  background-color: rgba(0, 0, 0, 0.253);
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  // opacity: 30%;
}

#menu-button {
  width: 50px;
  position: fixed;
  top: 10px;
  right: 10px;
  cursor: pointer;
  mix-blend-mode: difference;
  filter: invert(1);
  z-index: 5;
}

html {
  background-color: $bg2;
  overflow-x: hidden;
  &::before {
    content: "";
    position: absolute;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    width: 100%;
    height: 5000px;
    background-color: $bg1;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='60' height='60' viewBox='0 0 40 40'%3E%3Cg fill-rule='evenodd'%3E%3Cg fill='%239C92AC' fill-opacity='0.1'%3E%3Cpath d='M0 38.59l2.83-2.83 1.41 1.41L1.41 40H0v-1.41zM0 1.4l2.83 2.83 1.41-1.41L1.41 0H0v1.41zM38.59 40l-2.83-2.83 1.41-1.41L40 38.59V40h-1.41zM40 1.41l-2.83 2.83-1.41-1.41L38.59 0H40v1.41zM20 18.6l2.83-2.83 1.41 1.41L21.41 20l2.83 2.83-1.41 1.41L20 21.41l-2.83 2.83-1.41-1.41L18.59 20l-2.83-2.83 1.41-1.41L20 18.59z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
    z-index: -1;
    overflow: hidden;
    // transform: rotate(45deg);

    //parallax
    background-attachment: fixed;
    background-position: center;
    background-repeat: repeat;
  }
}

// body,
// #app {
//   height: 100%;
// }

// #root {
//   // padding: 60px;
//   height: 200%;
// }
</style>
