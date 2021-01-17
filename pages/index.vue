<template>
  <section class="container">
    <b-play-header/>
    <b-play-about-us/>
    <b-play-product/>
    <b-play-parterns/>
    <b-play-clients/>
  </section>
</template>

<script>
import BPlayHeader from '~/components/BPlayHeader.vue';
import BPlayAboutUs from '~/components/BPlayAboutUs.vue';
import BPlayProduct from '~/components/BPlayProduct.vue';
import BPlayParterns from '~/components/BPlayParterns.vue';
import BPlayClients from '~/components/BPlayClients.vue';

export default {
  components: {
    BPlayHeader,
    BPlayAboutUs,
    BPlayProduct,
    BPlayParterns,
    BPlayClients
  }
}
</script>

<style lang="scss" scoped>
* {
  padding: 0p;
  margin: 0;
}

.container {
  background-color: #15161D;
  color: #FDFDFD;
}
</style>

