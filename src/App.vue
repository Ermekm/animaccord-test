<template>
  <MyButton link="https://www.google.com/"> Google</MyButton>
  <MyButton link="https://www.google.com/"> Google</MyButton>
  <back-icon></back-icon>
</template>

<script>
import MyButton from "./components/MyButton.vue";
import BackIcon from "./components/icons/BackIcon.vue";

export default {
  name: "App",
  components: { MyButton, BackIcon },
};
</script>

<style>
@import "./assets/css/fonts.css";

body {
  background: #1e1e1e;
}

#app {
  font-family: "nunito", sans-serif;
}
</style>
