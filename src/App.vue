<template>
  <div>
    <div class="wrapper">
      <div class="col">
        <MyButton link="https://www.google.com/"> Google</MyButton>
        <MyButton link="https://www.google.com/"> Google</MyButton>
      </div>
      <div class="col">
        <MyButton color="primary" :icon="true" class="btn">
          <back-icon></back-icon>
        </MyButton>
        <MyButton color="danger" :icon="true" class="btn">
          <exit-icon></exit-icon>
        </MyButton>
        <MyButton color="tertiary" :icon="true" class="btn">
          <quest-icon></quest-icon>
        </MyButton>
        <MyButton color="primary" :icon="true" class="btn">
          <arrow-icon></arrow-icon>
        </MyButton>
        <MyButton color="danger" :icon="true" class="btn">
          <google-icon></google-icon>
        </MyButton>
        <MyButton color="info" :icon="true" class="btn">
          <vk-icon></vk-icon>
        </MyButton>
        <MyButton color="action" :icon="true" class="btn">
          <ok-icon></ok-icon>
        </MyButton>
        <MyButton color="primary" :icon="true" class="btn">
          <pen-icon></pen-icon>
        </MyButton>
      </div>
      <div class="col">
        <MyButton :countdown="181">Повторное письмо</MyButton>
      </div>
      <div class="col">
        <MyButton :color="color" v-for="color in colors" :key="color">
          Отправить письмо
        </MyButton>
        <MyButton disabled>Отправить письмо</MyButton>
      </div>
    </div>
  </div>
</template>

<script>
import MyButton from "./components/MyButton.vue";

import BackIcon from "./components/icons/BackIcon.vue";
import ExitIcon from "./components/icons/ExitIcon.vue";
import ArrowIcon from "./components/icons/ArrowIcon.vue";
import QuestIcon from "./components/icons/QeustIcon.vue";
import GoogleIcon from "./components/icons/GoogleIcon.vue";
import VkIcon from "./components/icons/VkIcon.vue";
import OkIcon from "./components/icons/OkIcon.vue";
import PenIcon from "./components/icons/PenIcon.vue";

export default {
  name: "App",
  components: {
    BackIcon,
    ExitIcon,
    QuestIcon,
    GoogleIcon,
    MyButton,
    ArrowIcon,
    VkIcon,
    OkIcon,
    PenIcon,
  },
  data() {
    return {
      colors: ["primary", "secondary", "warning", "info", "danger", "action"],
    };
  },
};
</script>

<style>
@import "./assets/css/fonts.css";
@import "./assets/css/reset.css";

body {
  background: #1e1e1e;
}

#app {
  font-family: "nunito", sans-serif;
}

.wrapper {
  display: flex;
  justify-content: space-between;
  margin: 30px 30px 0 30px;
}

.col {
  display: flex;
  flex-direction: column;
  margin: 0 10px;
}

.btn {
  margin-bottom: 14px;
}
</style>
