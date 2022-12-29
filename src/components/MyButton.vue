<template>
  <button :class="classArray" class="btn">
    <slot>Кнопка</slot>
  </button>
</template>

<script>
export default {
  name: "MyButton",
  props: {
    color: {
      type: String,
      default: "primary",
    },
    icon: {
      type: Boolean,
      default: false,
    },
  },
  computed: {
    classArray() {
      let baseClasses = [this.color];
      if (this.icon) {
        baseClasses.push("icon-wrapper");
      }
      return baseClasses;
    },
  },
};
</script>

<style scoped>
.btn {
  border: none;
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
</style>
