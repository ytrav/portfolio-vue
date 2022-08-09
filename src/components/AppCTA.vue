<template>
  <div id="CTA">
    <h1>Hi, I'm Anton</h1>
    <p>
      Front-End software developer<br />
      based in Hanover, Germany. I create seamless web apps using Vue.js and
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


#CTA {
  margin-top: 50px;
}


h1 {
  font-family: "Kanit", Verdana, Geneva, Tahoma, sans-serif;
  font-weight: medium;
  color: $primary;
  line-height: 40px;
}
p {
  font-family: "Poppins", Verdana, Geneva, Tahoma, sans-serif;
  font-weight: medium;
  // width: 360px;
  max-width: 360px;
  min-width: 175px;
  line-height: 30px;
  color: $primary;
}
#ctas {
  display: flex;
  justify-content: stretch;
  // width: 360px;
  max-width: 360px;
  min-width: 114px;
  flex-wrap: wrap;
  margin-top: 15px;
  gap: 15px;
  a {
    min-width: 100px;
    border-radius: 500px;
    flex-grow: 1;
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
        background-color: #004b91;
        // color: $primary;
        // filter: brightness(1.25);
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
}

// @media only screen and (max-width: 914px) {
//   #CTA {
//     margin-top: -150px;
//   }
// }
</style>
