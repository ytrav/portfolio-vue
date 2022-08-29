<template>
  <div id="landing">
    <AppHeader />
    <div id="headcta">
      <AppCTA />
    </div>
    <div id="img">
      <img src="../assets/portrait.png" alt="portrait" />
    </div>
  </div>
</template>

<script>
import AppCTA from "./AppCTA.vue";
import AppHeader from "./AppHeader.vue";

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
    AppHeader,
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
  padding: 60px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 82vh;

  // background-color: $bg1;
  // background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='60' height='60' viewBox='0 0 40 40'%3E%3Cg fill-rule='evenodd'%3E%3Cg fill='%239C92AC' fill-opacity='0.1'%3E%3Cpath d='M0 38.59l2.83-2.83 1.41 1.41L1.41 40H0v-1.41zM0 1.4l2.83 2.83 1.41-1.41L1.41 0H0v1.41zM38.59 40l-2.83-2.83 1.41-1.41L40 38.59V40h-1.41zM40 1.41l-2.83 2.83-1.41-1.41L38.59 0H40v1.41zM20 18.6l2.83-2.83 1.41 1.41L21.41 20l2.83 2.83-1.41 1.41L20 21.41l-2.83 2.83-1.41-1.41L18.59 20l-2.83-2.83 1.41-1.41L20 18.59z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
  // // z-index: -1;
  // // overflow: hidden;
  // // transform: rotate(45deg);

  // //parallax
  // background-attachment: fixed;
  // background-position: center;
  // background-repeat: repeat;
  // &::before {
  //   content: "";
  //   position: absolute;
  //   top: 0;
  //   left: 0;
  //   right: 0;
  //   bottom: 0;

  //   background-color: $bg1;
  //   background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='60' height='60' viewBox='0 0 40 40'%3E%3Cg fill-rule='evenodd'%3E%3Cg fill='%239C92AC' fill-opacity='0.1'%3E%3Cpath d='M0 38.59l2.83-2.83 1.41 1.41L1.41 40H0v-1.41zM0 1.4l2.83 2.83 1.41-1.41L1.41 0H0v1.41zM38.59 40l-2.83-2.83 1.41-1.41L40 38.59V40h-1.41zM40 1.41l-2.83 2.83-1.41-1.41L38.59 0H40v1.41zM20 18.6l2.83-2.83 1.41 1.41L21.41 20l2.83 2.83-1.41 1.41L20 21.41l-2.83 2.83-1.41-1.41L18.59 20l-2.83-2.83 1.41-1.41L20 18.59z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
  //   z-index: -1;
  //   overflow: hidden;
  //   // transform: rotate(45deg);

  //   //parallax
  //   background-attachment: fixed;
  //   background-position: center;
  //   background-repeat: repeat;
  // }
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
.landing-grid {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 0.4fr 1fr 1.3fr 1.3fr;
  gap: 0px 0px;
  grid-auto-flow: row;
  align-items: center;
  height: 91vh;
  padding: 60px;
  grid-template-areas:
    "h-g . img-g"
    ". . img-g"
    "cta-g . img-g"
    ". . img-g";
}

.cta-g {
  grid-area: cta-g;
}

.h-g {
  grid-area: h-g;
}

.img-g {
  grid-area: img-g;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;

  img {
    zoom: 100%;
    object-fit: cover;
  }
}

@media only screen and (max-width: 852px) {
  #landing {
    flex-direction: column-reverse;
    align-items: flex-start;
    height: auto;
  }

  #img {
    align-self: center;
  }

  #headcta {
    height: fit-content;
  }
}

// dont render #img if screen width smaller than 360px

@media only screen and (max-width: 360px) {
  #img {
    display: none;
  }
}

</style>