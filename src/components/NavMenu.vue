<template>
  <nav>
    <a @click="closeMenu" class="selected" href="#">Home</a>
    <a @click="closeMenu" href="#about-me">About me</a>
    <a @click="closeMenu" href="#skills">Skill set</a>
    <a @click="closeMenu" href="#exp">Experience</a>
    <a @click="closeMenu" href="#">Projects</a>
    <a @click="closeMenu" href="#">Contact</a>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      open: false,
    };
  },
  methods: {
    closeMenu() {
      this.$emit("closeMenu", false);
    },
  },
};
</script>

<style lang="scss" scoped>
$primary: #00315f;
$bg1: #efffff;
$bg2: #e3f5f7;

nav {
  position: fixed;
  right: 0;
  top: 0;
  bottom: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 40px;
  font-size: 1.2em;
  text-align: center;
  padding: 0 50px 0 50px;
  background-color: $bg1;
  border-radius: 10px 0 0 10px;
  // width: 107px;

  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
  a {
    text-decoration: none;
    color: $primary;
    width: 150px;
    height: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 10px;
    &:hover {
      color: #12538f;
      background-color: $bg2;
    }
  }
  // .selected::after {
  //     content: "l";
  //     height: 100%;
  //     width: 1px;
  //     background-color: $primary;
  //     margin-left: 3px;
  // }
}

@media only screen and (max-width: 460px) {
  nav {
    left: 0;
    border-radius: 0;
    align-items: center;
    a {
        width: 70%;
    }
  }
}

@media (hover: none) {
  nav {
    a {
      background-color: $bg2;
    }
  }
}
</style>