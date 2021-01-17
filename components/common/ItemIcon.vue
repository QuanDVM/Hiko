<template>
  <i :style="[styleIcon, { width: `${width}px`, height: `${height}px`, background: `url(${url})`, backgroundRepeat: 'no-repeat'}]" class="icon"></i>
</template>

<script>

export default {
  props: {
    width: {
      type: String,
      required: false,
      default: '',
    },
    height: {
      type: String,
      required: false,
      default: '',
    },
    url: {
      type: String,
      required: false,
      default: '',
    },
    styleIcon: {
      type: String,
      required: false,
      default: '',
    }
  },
  computed: {
  },
};
</script>

<style scoped>
.icon {
  display: inline-block;
}
</style>