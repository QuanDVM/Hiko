<template>
  <div class="scroll" :style="styleScroll">
    <div v-if="postionText === 'top'">
      <p class="scroll__text">{{text}}</p>
      <img src="../../static/images/scrollBottom.png" alt="logo" class="scroll__icon">
    </div>
    <div v-if="postionText === 'bottom'">
      <img src="../../static/images/scrollTop.png" alt="logo" class="scroll__icon">
      <p class="scroll__text">{{text}}</p>
    </div>
  </div>
</template>

<script>

export default {
  props: {
    styleScroll: {
      type: Object,
      required: false
    },
    text: {
      type: String,
      required: true,
      default: 'text'
    },
    postionText: {
      type: String,
      required: true,
      default: 'top'
    }
  }
}
</script>

<style lang="scss" scoped>
.scroll {
  width: 85px;
  text-align: center;
  color: #FFFFFF;

  &__text {
    font-size: 30px;
    text-align: center;
  }

  &__icon {
    width: 52px;
    height: 40px;
  }
}

@media only screen and (max-width: 480px) and (min-width: 320px){
  .scroll {
    font-size: 12px;
  }
}
</style>