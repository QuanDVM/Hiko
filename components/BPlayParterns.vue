<template>
  <div class="parterns">
    <img src="../static/images/partners.png" alt="" class="parterns__img isPc" />
    <img src="../static/images/partners.png" alt="" class="parterns__img isSp" />
    <div class="parterns__info">
      <div class="parterns__description">
        <info-description
          nameCompany="BPLAY GAME"
          title="PARTNERS"
          text="As a BPlay client you will benefit from content from more than 20 top tier providers. Based on your casino’s concept and targeted markets, we will tailor the perfect portfolio of games to offer to your players."
          :textCenter="false"
        />
      </div>
      <group-image 
        :styleImage="{ width: '150px'}"
        :listImage="['hogaming', 'iovation', 'sbtech', 'seon', 'vivo']"
        :islistImageCenter="true"
      />
    </div>
  </div>
</template>
<script>
import InfoDescription from '~/components/InfoDescription.vue';
import GroupImage from '~/components/items/GroupImage.vue';

export default {
  components: {
    InfoDescription,
    GroupImage,
  },
}
</script>

<style lang="scss" scoped>
.parterns {
  display: flex;
  align-items: center;

  &__info {
    margin-left: 60px;
    width: 620px;
  }

  &__description {
    margin: 0 auto;
    padding: 0 60px;
  }

  &__img {
    margin-top: 20px;
    width: 535px;
  }
}

.isPc {
  display: block;
}

.isSp {
  display: none;
}

@media only screen and (max-width: 480px) and (min-width: 320px){
  .parterns {
    flex-direction: column-reverse;

    &__info {
      margin-left: 0;
      margin: 0 auto;
      width: auto;
    }

    &__description {
      width: auto;
      padding: 0 10px;
    }

    &__img {
      width: 100%;
    }
  }

  .isPc {
    display: none;
  }

  .isSp {
    display: block;
  }
}
</style>