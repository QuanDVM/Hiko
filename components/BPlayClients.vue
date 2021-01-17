<template>
  <div class="clients">
    <div class="clientsContent">
      <info-description
        nameCompany="BPLAY GAME"
        title="OUR CLIENTS"
      />
      <div class="clientsContent__info">
        <group-image 
          :styleImage="{ width: '150px'}"
          :listImage="['00', '01', '02', '03', '04', '05', '06', '07', '08', '09', '10', '11']"
          :islistImageCenter="true"
        />
      </div>
      <b-play-footer/>
      <item-scroll
        :styleScroll="{
        transform: 'translate(-50%, -50%)',
          position: 'absolute',
          right: '5%',
          bottom: '0'
        }"
        text="Top"
        postionText="bottom"
      />
    </div>
  </div>
</template>

<script>
import InfoDescription from '~/components/InfoDescription.vue';
import BPlayFooter from '~/components/BplayFooter.vue';
import GroupImage from '~/components/items/GroupImage.vue';
import ItemScroll from '~/components/items/ItemScroll.vue';

export default {
  components: {
    InfoDescription,
    GroupImage,
    BPlayFooter,
    ItemScroll
  },
}
</script>

<style lang="scss" scoped>
.clients {
  background-image: url("../static/images/footer.png");
  background-size: 100%;
  background-repeat: no-repeat;
  background-position: left bottom;
  position: relative;
}
.clientsContent {
  max-width: 900px;
  margin: 0 auto;

  &__info {
    margin-top: 10px;
  }
}

@media only screen and (max-width: 480px) and (min-width: 320px){
  .clients {
    background-image: url("../static/images/footerSp.png");
    background-size: 100%;
    background-repeat: no-repeat;
    background-position: left bottom;
  }
}
</style>