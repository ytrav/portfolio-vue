<template>
  <div id="landing">
    <AppCTA />
    <img src="../assets/portrait.png" alt="portrait" />
    <!-- <nav>
      <a href="#" @click="move('home')" :class="{ selected: isHome }">Home</a>
      <a @click="move('about')" :class="{ selected: isAbout }">About</a>
      <a @click="move('exp')" :class="{ selected: isExp }">Experience</a>
      <a @click="move('work')" :class="{ selected: isWork }">Work</a>
      <a @click="move('contacts')" :class="{ selected: isContacts }"
        >Contacts</a
      >
    </nav> -->
  </div>
</template>

<script>
import AppCTA from "./AppCTA.vue";

export default {
  data() {
    return {
      isHome: true,
      isAbout: false,
      isExp: false,
      isWork: false,
      isContacts: false,
    };
  },

  components: {
    AppCTA,
  },
  methods: {
    move(tab) {
      switch (tab) {
        case "home":
          this.isHome = true;
          this.isAbout = false;
          this.isExp = false;
          this.isWork = false;
          this.isContacts = false;
          break;
        case "about":
          this.isHome = false;
          this.isAbout = true;
          this.isExp = false;
          this.isWork = false;
          this.isContacts = false;
          break;
        case "exp":
          this.isHome = false;
          this.isAbout = false;
          this.isExp = true;
          this.isWork = false;
          this.isContacts = false;
          break;
        case "work":
          this.isHome = false;
          this.isAbout = false;
          this.isExp = false;
          this.isWork = true;
          this.isContacts = false;
          break;
        case "contacts":
          this.isHome = false;
          this.isAbout = false;
          this.isExp = false;
          this.isWork = false;
          this.isContacts = true;
          break;
        default:
          break;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
$primary: #00315f;
$bg1: #efffff;
$bg2: #e3f5f7;

img {
  max-width: 360px;
}

#landing {
  display: flex;
  align-items: center;
  justify-content: space-between;
  justify-items: center;
  // flex-wrap: wrap-reverse;
  // height: 50%;
  // border: 1px solid red;
  // margin-top: -70px;
  // background-image: url("./../assets/lightbg.svg");
  // background-image: url("");
  // background-repeat: repeat;
  &::before {
    content: "";
    position: absolute;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    background-color: $bg1;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='60' height='60' viewBox='0 0 40 40'%3E%3Cg fill-rule='evenodd'%3E%3Cg fill='%239C92AC' fill-opacity='0.1'%3E%3Cpath d='M0 38.59l2.83-2.83 1.41 1.41L1.41 40H0v-1.41zM0 1.4l2.83 2.83 1.41-1.41L1.41 0H0v1.41zM38.59 40l-2.83-2.83 1.41-1.41L40 38.59V40h-1.41zM40 1.41l-2.83 2.83-1.41-1.41L38.59 0H40v1.41zM20 18.6l2.83-2.83 1.41 1.41L21.41 20l2.83 2.83-1.41 1.41L20 21.41l-2.83 2.83-1.41-1.41L18.59 20l-2.83-2.83 1.41-1.41L20 18.59z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
    z-index: -1;
    // transform: rotate(45deg);

    //parallax
    background-attachment: fixed;
    background-position: center;
    background-repeat: repeat;
  }
}
nav {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  color: $primary;
  position: fixed;
  right: 70px;
  mix-blend-mode: difference;
  filter: invert(1);
  a {
    text-align: center;
    text-decoration: none;
    color: inherit;
  }
  .selected::after {
    content: "\00a0";
    position: relative;
    right: -10px;
    width: 2px;
    height: 5px;
    background-color: $primary;
  }
}
// #landing::after {
//   display: block;
//   position: absolute;
//   content: "";
//   top: 0;
//   left: 0;
//   right: 0;
//   bottom: 0;
//   // background-image: url("./../assets/lightbg.svg");
// }

// @media only screen and (max-width: 914px) {
//   #landing {
//     flex-direction: column-reverse;
//     align-items: flex-start;
//   }
//   // img {
//   //   margin-left: 210px;
//   // }

// }
</style>