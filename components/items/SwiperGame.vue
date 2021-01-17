<template>
  <div class="swiper-container isSp">
      <!-- Additional required wrapper -->
      <div class="swiper-wrapper">
          <!-- Slides -->
          <div class="swiper-slide" v-for="(game, index) in listGame" :key="index" >
            <item-game :game="game"/>
          </div>
      </div>
      <!-- If we need pagination -->
      <div class="swiper-pagination"></div>
  </div>
</template>

<script>
import Swiper, { Navigation, Pagination } from 'swiper';
import 'swiper/swiper-bundle.css';
import ItemGame from '~/components/items/ItemGame.vue';

Swiper.use([ Navigation, Pagination ])

export default {
  components: {
    ItemGame
  },
  props: {
    listGame: {
      type: Array,
      required: true
    },
  },
  mounted() {
    new Swiper('.swiper-container', {
      slidesPerView: 'auto',
      spaceBetween: 30,
      pagination: {
        el: '.swiper-pagination',
        clickable: true
      },
    })
  }
}
</script>

<style lang="scss" scoped>
.swiper-container {
  width: 100%;
  height: 100%;
  padding-bottom: 20px;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  width: 80%;

  /* Center slide text vertically */
  display: -webkit-box;
  display: flex;
  justify-content: center;
  align-items: center;
}

.swiper-slide {
  width: 60%;
}

.isSp {
  display: none;
}

@media only screen and (max-width: 480px) and (min-width: 320px){
  .isSp {
    display: block;
  }
}
</style>

<style lang="scss">
  .swiper-pagination-bullet {
    background: #505153;
    transform: rotate(45deg);
    width: 5px;
    height: 5px;
    border-radius: 0px;
  }

  .swiper-pagination-bullet.swiper-pagination-bullet-active {
    background: #F41616;
  }

  .swiper-container-horizontal > .swiper-pagination-bullets {
    bottom: 0;
  }
</style>

