<template>
  <div class="itemGame">
    <img :src="require(`~/assets/imgs/${game.nameImage}.png`)" class="itemGame__img">
    <div class="itemGame__action">
      <item-button>{{ game.name }}</item-button>
    </div>
    <p class="itemGame__description">{{ game.description }}</p>
  </div>
</template>

<script>
import ItemButton from '~/components/common/ItemButton'

export default {
  components: {
    ItemButton
  },
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

  &__action {
    margin-top: 26px;
  }
}
</style>