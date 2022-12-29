<template>
  <MyButton color="primary" :icon="true" class="btn">
    <back-icon></back-icon>
  </MyButton>
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
