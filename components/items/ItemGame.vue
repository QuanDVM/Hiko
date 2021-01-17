<template>
  <div class="itemGame">
    <img :src="require(`~/assets/imgs/${game.nameImage}.png`)" class="itemGame__img">
    <button class="buttonGame">{{ game.name }}</button>
    <p class="itemGame__description">{{ game.description }}</p>
  </div>
</template>

<script>
export default {
  props: {
    game: {
      type: Object,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.itemGame {
  &__img {
    width: 100%;
  }

  &__description {
    font-size: 14px;
    margin-top: 20px;
  }
}

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