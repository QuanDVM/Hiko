<template>
  <div :class="['groupImage', { 'islistImageCenter': islistImageCenter }]" :style="styleGroupImage">
    <a href="#"
      class="groupImage__item"
      v-for="(image, index) in listImage"
      :key="index"
    >
      <img
        :src="require(`~/assets/imgs/${image}.png`)"
        class="groupImage__img"
        :style="styleImage">
    </a>
  </div>
</template>

<script>
export default {
    props: {
      styleImage: {
        type: Object,
        required: false
      },
      styleGroupImage: {
        type: Object,
        required: false
      },
      listImage: {
        type: Array,
        required: true
      },
      islistImageCenter: {
        type: Boolean,
        required: false,
        default: false,
      },
    }
}
</script>

<style lang="scss" scoped>
.groupImage {
  display: flex;
  flex-wrap: wrap;

  &__item {
    display: block;
    margin: 5px;
  }
  &__img {
    width: 100%;
  }
}
.islistImageCenter {
  justify-content: center;
}
</style>