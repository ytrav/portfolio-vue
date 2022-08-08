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
      <path fill="url(#a)" fill-opacity=".05" d="M0-4h1920v965H0z" />
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
  margin-top: -70px;
  // background-image: url("./../assets/lightbg.svg");
  // background-image: url("");
  // background-repeat: repeat;
  &::before {
    content: "";
    position: absolute;
    top: -400px;
    bottom: -200px;
    right: -300px;
    left: -220px;
    background-color: $bg2;
    background-image: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%2300315f' fill-opacity='0.05'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
    z-index: -1;
    transform: rotate(45deg);
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