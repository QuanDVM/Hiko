<template>
  <div class="product">
    <info-description
      nameCompany="BPLAY GAME"
      title="OUR PRODUCTS"
      text="BPlay’s high quality iGaming Platform offers a complete solution for your casino. Get the full White Label turnkey solution or the Seamless API with our comprehensive selection of games. Through our global network of premium partners such as Vivo Gaming, SBTech and HoGaming you will have access to the best Live Casino, Sportsbook, Slots, Table Games, Number Games and Fishing Games on the market."
      :textCenter="false"
      :isDisplayHorizontal="true"
    />
    <list-game :listGame="listGame" />
  </div>
</template>
<script>
import InfoDescription from '~/components/InfoDescription.vue';
import ListGame from '~/components/items/ListGame.vue';

export default {
  components: {
    InfoDescription,
    ListGame
  },
  data() {
    return {
      listGame: [{
        nameImage: 'game1',
        name: 'Live Casino',
        description: 'Vivo LiveCasino, HoGaming Live Casino, BPlay LiveCasino'
      },
      {
        nameImage: 'game2',
        name: 'Fishing Game',
        description: 'BPlay Fishing 2D, BPlay Fishing 3D'
      },
      {
        nameImage: 'game3',
        name: 'Sport Book',
        description: 'BTI Sportsbook, BPlay Sportsbook'
      },
      {
        nameImage: 'game4',
        name: 'Quick Number',
        description: 'Keno, Number Games, Lottery'
      },
      {
        nameImage: 'game5',
        name: 'White Label',
        description: 'Bplay White Label'
      },
      {
        nameImage: 'game6',
        name: 'Slots',
        description: 'BPlay Slots, Jackpot Slots'
      },
      {
        nameImage: 'game7',
        name: 'Seamless API',
        description: 'Seamless API'
      },
      {
        nameImage: 'game8',
        name: 'Full Package',
        description: 'Full Package'
      },
      {
        nameImage: 'game9',
        name: 'Table Game',
        description: 'Table Game'
      },
      ]
    }
  },
}
</script>
<style lang="scss" scoped>
.product {
  background-image: url("../static/images/backgroudProduct.png"), url("../static/images/backgroudWave.png");
  background-size: 100%;
  background-repeat: no-repeat;
  padding: 228px 260px 330px;
  background-color: #15161e;
}
@media only screen and (max-width: 480px) and (min-width: 320px){
  .product {
    padding: 20px 0;
    background-image: url("../static/images/backgroudProduct.png"), url("../static/images/backgroudWaveSP.png");
    background-size: 100%;
    background-repeat: no-repeat;
  }
}
</style>