<template>
  <div class="listGame isPc">
    <item-game :game="game" v-for="(game, index) in listGame" :key="index" />
  </div>
</template>

<script>
import ItemGame from '~/components/items/ItemGame.vue';

export default {
  components: {
    ItemGame
  },
  props: {
    listGame: {
      type: Array,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.listGame {
  display: grid;
  grid-gap: 50px;
  grid-template-columns: auto auto auto;
  margin-top: 85px;
  text-align: center;
}

@media only screen and (max-width: 480px) and (min-width: 320px){
  .listGame {
    grid-template-columns: none;

    &.isPc {
      display: none;
    }
  }
}
</style>