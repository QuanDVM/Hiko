<template>
  <div class="aboutus">
    <div class="aboutus__info">
      <info-description
        nameCompany="BPLAY GAME"
        title="WHO WE ARE?"
        text="BPlay was founded in 2015 by a group of highly skilled professionals with over 15 years of experience in the iGaming industry. Today we are an international company with more than 100 employees and have operations in Malta, Ukraine, Romania, Norway, India, Myanmar and Taiwan..."
      />
    </div>
    <img src="../static/images/maps.png" alt="logo" class="aboutus__maps isPC">
    <img src="../static/images/mapsSP.png" alt="logo" class="aboutus__maps isSP">
    <div>
      <div class="labelExp">
        <p class="labelExp__numberYear isTextHight">15</p>
        <p class="labelExp__textYear">YEARS</p>
        <hr class="labelExp__line"/>
        <p class="labelExp__text">of experience<br/>in the <span class="isTextHight">iGaming</span></p>
      </div>
    </div>
  </div>
</template>

<script>
import InfoDescription from '~/components/InfoDescription.vue';

export default {
  components: {
    InfoDescription
  },
}
</script>

<style lang="scss" scoped>
.aboutus {
  text-align: center;
  background: url("../static/images/buildings.png");
  background-size: 100%;
  background-repeat: no-repeat;
  background-position: left bottom;
  position: relative;
  padding-bottom: 300px;

  &__info {
    max-width: 825px;
    margin: 0 auto;
  }

  &__maps {
    width: 100%;
  }
}

.labelExp {
  padding: 0 35px 45px;
  background: rgba(21, 22, 30, 0.9);
  border-radius: 0 0 20px 20px;
  left: 265px;
  position: absolute;
  bottom: 135px;

  &__numberYear {
    font-weight: bold;
    font-size: 100px;
  }

  &__textYear {
    font-weight: 600;
    font-size: 35px;
    color: #FFF;
  }

  &__text {
    font-size: 16px;
  }

  &__line {
    width: 70px;
    height: 1px;
    margin: 10px auto;
    color: #F41616;
  }
}

.isTextHight {
  color: #F41616;
}

.isPC {
  display: block;
}
.isSP {
  display: none;
}
@media only screen and (max-width: 480px) and (min-width: 320px){
  .aboutus {
    background: url("../static/images/buildingsSP.png");
    background-size: 100%;
    background-repeat: no-repeat;
    background-position: left bottom;
  }
  .isPC {
    display: none;
  }
  .isSP {
    display: block;
  }

  .labelExp {
    bottom: auto;
    left: 50%;
    top: 75%;
    transform: translate(-50%, -50%);
    padding: 0 35px 20px;
  }
}
</style>