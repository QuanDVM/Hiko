<template>
  <div
    :class="['infoDescription', {'isDisplayHorizontal': isDisplayHorizontal, 'textCenter': textCenter}]"
  >
    <div>
      <h5 class="infoDescription__nameCompany">{{ nameCompany }}</h5>
      <h3 class="infoDescription__title">{{ title }}</h3>
    </div>
    <p class="infoDescription__text" :style="{ width: widthText }" v-if="text">{{ text }}</p>
  </div>
</template>

<script>
export default {
  props: {
    nameCompany: {
      type: String,
      required: true,
      default: 'nameCompany'
    },
    title: {
      type: String,
      required: true,
      default: 'title'
    },
    text: {
      type: String,
      required: false,
      default: ''
    },
    widthText: {
      type: String,
      required: false,
      default: 'auto'
    },
    textCenter: {
      type: Boolean,
      required: false,
      default: true
    },
    isDisplayHorizontal: {
      type: Boolean,
      required: false,
      default: false
    }
  }
}
</script>

<style lang="scss" scoped>
.infoDescription {
  &__nameCompany {
    font-size: 20px;
    color: #FF3232;
  }

  &__title {
    font-weight: 800;
    font-size: 30px;
    color: #FDFDFD;
    margin-top: 8px;
  }

  &__text {
    font-size: 14px;
    color: #E6E6E6;
    margin-top: 32px;
  }

  &.isDisplayHorizontal {
    display: flex;
    & .infoDescription {
      &__title {
        margin-top: 0;
      }

      &__text {
        margin: 0;
        margin-left: 54px;
      }
    }
  }
}

.textCenter {
  text-align: center;
}

@media only screen and (max-width: 480px) and (min-width: 320px){
  .infoDescription {
    text-align: center;

    &.isDisplayHorizontal {
      display: block;

      & .infoDescription__text {
        margin-left: 0;
        margin-top: 32px;
      }
    }
  }
}
</style>