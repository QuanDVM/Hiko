<template>
  <header class="header">
    <div class="header__action">
      <img src="../static/images/logo.png" alt="logo" class="header__logo">
      <b-play-menu/>
    </div>
    <h1 class="header__heading">CASINO<br/>PLAYGAME</h1>
    <item-scroll :styleScroll="{
        transform: 'translate(-50%, -50%)',
        position: 'absolute',
        left: '50%',
        bottom: '15%'
      }"
      text="Scroll"
      postionText="top"
    />
  </header>
</template>

<script>
import BPlayMenu from '~/components/BPlayMenu.vue';
import ItemScroll from '~/components/items/ItemScroll.vue';

export default {
  components: {
    BPlayMenu,
    ItemScroll,
  },
}
</script>

<style lang="scss" scoped>
.header {
  background-image: url("../static/images/banner.png");
  background-size: 100%;
  background-repeat: no-repeat;
  height: 850px;
  position: relative;

  &__action {
    display: flex;
    max-width: 900px;
    justify-content: space-between;
    margin: 0 auto;
    padding: 10px 0;
  }

  &__heading {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    font-weight: 800;
    font-size: 96px;
    text-shadow: 0px 0px 50px rgba(0, 0, 0, 0.4);
    text-align: center;
    letter-spacing: 10px;
    animation: fadeIn 2s;
    animation-delay: 0.5s;
  }

  &__logo {
    width: 152px;
  }
}

@keyframes fadeIn {
  0% {
    top: 55%;
    opacity: 0;
  }
  50% {
    top: 48%;
    opacity: 0.8;
  }
  100% {
    top: 50%;
    opacity: 1;
  }
}
@media only screen and (max-width: 480px) and (min-width: 320px){
  .header {
    background-image: url("../static/images/bannerSP.png");
    height: 460px;

    &__logo {
      width: 100px;
      padding-left: 10px;
    }

    &__heading {
      font-size: 36px;
    }
  }
}
</style>