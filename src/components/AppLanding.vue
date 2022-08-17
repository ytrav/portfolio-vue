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
</style>