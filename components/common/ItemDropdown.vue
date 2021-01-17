<template id="dropdown">
  <div class="my-dropdown">
    <div class="selected" @click="toggle" v-html="selected"></div>
    <div class="options" v-show="isOpen">
      <div
        class="option"
        v-for="(option, index) in options"
        @click="set(option)"
        :key="index"
        v-html="option"
      >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    options: {
      type: Array,
      required: true
    }
  },
  data() {
    return {
      isOpen: false,
      selected: '',
    }
  },
  mounted() {
    this.selected = this.options[0];
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen;
    },
    show() {
      this.isOpen = true;
    },
    hide() {
      this.isOpen = false;
    },
    set(option) {
      this.selected = option;
      this.hide();
    }
  },
}
</script>

<style scoped>
/* My dropdown */
.my-dropdown {
  cursor: pointer;
  position: relative;
  display: inline-block;
}

/* Selected */
.selected {
  position: relative;
  z-index: 2;
  display: flex;
  align-items: center;
  width: 100%;
  padding: 5px 10px;
  border-radius: 100px;
  border: 0.5px solid #FFFFFF;
  color: #fff;
}

/* Arrow */
.selected:after {
  opacity: 0.5;
  display: inline-block;
  margin-left: 10px;
  content: url('../../static/images/triangle.png');
}

/* Hover state */
.selected:hover:after {
  opacity: 1;
}

/* Options wrapper (toggled by isOpen) */
.options {
  position: absolute;
  left: 0;
  top: 100%;
  z-index: 1;
  width: 100%;
  margin-top: 3px;
  border-radius: 100px;
}

.option {
  padding: 3px 10px;
  border-bottom: 1px solid rgba(0, 0, 0, 0.25);
  font-size: 12px;
  border-radius: 100px;
  border: 0.5px solid #FFFFFF;
  display: flex;
  align-items: center;
}

.option:hover {
  background-color: rgba(0, 0, 0, 0.05);
}

.fade-enter-active, .fade-leave-active {
  transition: all .25s ease-out;
}

.fade-enter, .fade-leave-active {
  opacity: 0;
	transform: translateY(-30px);
}
</style>