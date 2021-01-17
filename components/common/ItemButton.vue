<template>
  <button class="buttonGame" :disabled="disabled" :style="styles"><slot></slot></button>
</template>

<script>
export default {
  props: {
    disabled: {
      type: Boolean,
      required: false,
      default: false,
    },
    styles: {
      type: Boolean,
      required: false
    }
  }
}
</script>
<style scoped>
.buttonGame {
  width: 170px;
  height: 30px;
  background: url("../../static/images/frame.png");
  background-size: 100%;
  background-repeat: no-repeat;
  outline: none;
  border: none;
  font-size: 16px;
  color: #FFFDF1;
}
</style>