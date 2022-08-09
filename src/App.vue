<template>
  <div id="root">
    <AppHeader />
    <AppLanding />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppLanding from "./components/AppLanding.vue";
// import LightBG from "src/assets/"

export default {
  name: "App",
  components: {
    AppHeader,
    AppLanding,
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
  border: 1px solid rgba(255, 0, 0, 0.479);
}

html {
  background-color: $bg2;
  height: 100%;
  overflow-x: hidden;
}

body,
#app {
  height: 100%;
}

#root {
  padding: 60px;
  height: 200%;
}
</style>
