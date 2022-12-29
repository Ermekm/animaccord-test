<template>
  <MyButton color="primary" class="btn"></MyButton>
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

#app {
  font-family: "nunito";
}
</style>
