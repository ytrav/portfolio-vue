<template>
  <div id="landing">
    <AppCTA />
    <svg
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
      width="1920"
      height="961"
      fill="none"
      viewBox="0 0 1920 961"
    >
      <path fill="url(#a)" fill-opacity=".5" d="M0-4h1920v965H0z" />
      <defs>
        <pattern
          id="a"
          width=".042"
          height=".083"
          patternContentUnits="objectBoundingBox"
        >
          <use xlink:href="#b" transform="scale(.00052 .00104)" />
        </pattern>
      </defs>
    </svg>
  </div>
</template>

<script>
import AppCTA from "./AppCTA.vue";

export default {
  components: {
    AppCTA,
  },
};
</script>

<style lang="scss" scoped>
$primary: #00315f;
$bg1: #efffff;
$bg2: #e3f5f7;

#landing {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  height: 50%;
  border: 1px solid red;
  margin-top: -70px;
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
    background-color: $bg2;
background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='60' height='60' viewBox='0 0 40 40'%3E%3Cg fill-rule='evenodd'%3E%3Cg fill='%239C92AC' fill-opacity='0.1'%3E%3Cpath d='M0 38.59l2.83-2.83 1.41 1.41L1.41 40H0v-1.41zM0 1.4l2.83 2.83 1.41-1.41L1.41 0H0v1.41zM38.59 40l-2.83-2.83 1.41-1.41L40 38.59V40h-1.41zM40 1.41l-2.83 2.83-1.41-1.41L38.59 0H40v1.41zM20 18.6l2.83-2.83 1.41 1.41L21.41 20l2.83 2.83-1.41 1.41L20 21.41l-2.83 2.83-1.41-1.41L18.59 20l-2.83-2.83 1.41-1.41L20 18.59z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
    z-index: -1;
    // transform: rotate(45deg);
  }
}

svg {
  fill: black;
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
</style>