<template>
  <button class="button-link" v-if="link">
    <a :href="link" class="link"><slot></slot></a>
  </button>
  <button :class="classArray" class="btn" @click="refreshTimer" v-else>
    <slot>Кнопка</slot>
    <span class="timer-wrapper" v-if="countdown">
      {{ timer }}
    </span>
  </button>
</template>

<script>
export default {
  name: "MyButton",
  mounted() {
    this.countDownTimer();
  },
  props: {
    color: {
      type: String,
      default: "primary",
    },
    icon: {
      type: Boolean,
      default: false,
    },
    countdown: {
      type: Number,
    },
    link: {
      type: String,
    },
  },
  computed: {
    classArray() {
      let baseClasses = [this.color];
      if (this.icon) {
        baseClasses.push("icon-wrapper");
      }
      if (this.timerCount === 0) {
        baseClasses.push("timer_over");
      } else if (this.timerCount > 0) {
        baseClasses.push("timer");
      }
      return baseClasses;
    },
    timer() {
      const minutes =
        Math.floor(this.timerCount / 60) < 10
          ? "0" + Math.floor(this.timerCount / 60)
          : Math.floor(this.timerCount / 60);

      const seconds =
        this.timerCount % 60 < 10
          ? "0" + (this.timerCount % 60)
          : this.timerCount % 60;

      return minutes + ":" + seconds;
    },
  },
  data() {
    return {
      timerCount: this.countdown,
    };
  },
  methods: {
    countDownTimer() {
      if (this.timerCount > 0) {
        setTimeout(() => {
          this.timerCount--;
          this.countDownTimer();
        }, 1000);
      }
    },
    refreshTimer() {
      if (this.timerCount === 0) {
        this.timerCount = this.countdown;
        this.countDownTimer();
      }
    },
  },
};
</script>

<style scoped>
.btn {
  border: none;
  font-family: "nunito";
  font-size: 18px;
  line-height: 24px;
  text-transform: uppercase;
  color: #fff;
  fill: #fff;
  padding: 14px 46px;
  white-space: nowrap;
  border-radius: 15px 15px 20px 15px / 15px 25px 30px 25px;
}

.icon-wrapper {
  padding: 15px;
}

.primary {
  background-color: #702c7e;
}

.secondary {
  background-color: #c4296c;
}

.tertiary {
  background-color: #6dd1b0;
}

.warning {
  background-color: #f4ba46;
}

.disabled {
  background-color: #efefef;
  color: #767679;
  fill: #767679;
}

.info {
  background-color: #0083b6;
}

.danger {
  background-color: #df3f3e;
}

.action {
  background-color: #ed732e;
}

.btn:disabled {
  background-color: #efefef;
  color: #767679;
  fill: #767679;
}

/* timer styles start*/
.btn.timer {
  background-color: #efefef;
  color: #767679;
  fill: #767679;
}

.btn.timer_over {
  background-color: #702c7e;
  color: #fff;
}

.timer-wrapper {
  padding: 6px;
  margin-left: 6px;
  background-color: #df3f3e;
  color: #fff;
  border-radius: 10px 15px 20px 15px / 15px 25px 30px 25px;
}
/* timer styles end */

/* link styles start */
.button-link {
  background: transparent;
  border: none;
}

.link {
  color: #fff;
  font-family: "Nunito";
  font-weight: bold;
}

.link:hover {
  color: #767679;
}

.link:active {
  color: #c4296c;
}
/* link styles end */

@media (max-width: 639px) {
  .btn {
    font-size: 12px;
    line-height: 24px;
    text-transform: uppercase;
    color: #fff;
    fill: #fff;
    padding: 6px 16px;
    box-sizing: border-box;
  }

  .btn.icon-wrapper {
    padding: 14px;
  }
}
</style>
