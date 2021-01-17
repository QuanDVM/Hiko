<template>
  <button class="buttonGame"><slot></slot></button>
</template>

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
  margin-top: 26px;
}
</style>