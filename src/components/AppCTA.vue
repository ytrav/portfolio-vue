<template>
  <div>
    <h1>Hi, I'm Anton</h1>
    <p>
      Front-End software developer<br />
      based in Hanover, Germany. Creating seamless web apps using Vue.js and
      Sass
    </p>
    <div id="ctas">
      <a>Contact me</a>
      <a>Projects</a>
    </div>
  </div>
</template>

<style lang="scss" scoped>
$primary: #00315f;
$bg1: #efffff;
$bg2: #e3f5f7;

h1 {
  font-family: "Kanit", Verdana, Geneva, Tahoma, sans-serif;
  font-weight: medium;
}
p {
  font-family: "Poppins", Verdana, Geneva, Tahoma, sans-serif;
  font-weight: medium;
  width: 360px;
  line-height: 30px;
}
#ctas {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  width: 360px;
  margin-top: 15px;
}
a {
  width: 170px;
  border-radius: 500px;
  border: 2px solid $primary;
  padding: 10px;
  font-size: 1.1em;
  text-align: center;
  cursor: pointer;
  background-color: $bg1;
  transition: background-color 0.2s ease-out, filter 0.05s ease-out;
  &:nth-child(1) {
    background-color: $primary;
    color: $bg1;
    &:hover {
      background-color: $bg1;
      color: $primary;
    }
  }
  &:nth-child(2) {
    background-color: $bg1;
    color: $primary;
    &:hover {
      // filter: brightness(0.9);
      background-color: $bg2;
    }
    &:active {
      filter: brightness(0.85);
    }
  }

  &:active {
    filter: brightness(0.85);
  }
}
</style>