<template>
  <div class="footer">
    <div class="footer__contact">
      <div class="footer__logo">
        <img src="../static/images/logo.png" alt="logo" width="150">
      </div>
      <div class="footer__contactus">
        <p class="footer__contactTitle">CONTACT US</p>
        <ul class="detailContact">
          <li class="detailContact__item">
            <span><item-icon width="30" height="20" url="/images/local.svg"/></span>
            <span class="detailContact__content">2901 Marmora Road, Glassgow, Seattle,<br/>WA 98122-1090</span>
          </li>
          <li class="detailContact__item">
            <span><item-icon width="24" height="30" url="/images/email.svg"/></span>
            <span class="detailContact__content">info@bplay.com</span>
            </li>
        </ul>
      </div>
    </div>
    <div class="footer__copyright">
      <div class="footer__listlogo">
        <img src="../static/images/license1.png" alt="" width="170" class="footer__logoLicense" />
        <img src="../static/images/license2.png" alt="" width="58" class="footer__logoLicense" />
        <img src="../static/images/license3.png" alt="" width="38" class="footer__logoLicense" />
        <img src="../static/images/license4.png" alt="" width="44" class="footer__logoLicense" />
      </div>
      <p class="footer__textCopyright">Copyright © 2020 bplay.com. All rights reserved.</p>
    </div>
  </div>
</template>

<script>
import ItemIcon from '~/components/common/ItemIcon.vue';

export default {
  components: {
    ItemIcon
  },
}
</script>

<style lang="scss" scoped>
.footer {
  margin-top: 100px;
  max-width: 900px;
  position: relative;

  &__contact {
    display: flex;
    padding: 50px 0;
  }

  &__logo, &__contactus {
    width: 50%;
  }

  &__contactTitle {
    color: #FDFDFD;
    font-weight: 800;
    font-size: 34px;
  }

  &__copyright {
    padding: 10px 0;
    border-top: 0.5px solid #424657;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  &__textCopyright {
    font-size: 14px;
  }

  &__listlogo {
    padding-left: 5px;
  }
  &__logoLicense {
    margin-right: 20px;

    &:first-child {
      margin-right: 10px;
    }

    &:last-child {
      margin-right: 0;
    }
  }
}

.detailContact {
  margin-top: 5px;
  padding: 0;

  &__item {
    list-style: none;
    display: flex;
    align-items: center;
  }

  &__content {
    margin-left: 10px;
  }
}

@media only screen and (max-width: 480px) and (min-width: 320px){
  .footer {
    padding: 0 10px;
    &__contact {
      display: block;
    }

    &__logo {
      width: auto;
    }

    &__contactus {
      margin-top: 10px;
      width: auto;
    }

    &__copyright {
      flex-direction: column;
    }

    &__listlogo {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-around;
      margin-top: 10px;
      padding-left: 0;
      padding-bottom: 10px;
    }

    &__logoLicense {
      margin-right: 0;
    }

    &__logoLicense:first-child {
      order: 1;
      margin-top: 20px;
    }

    &__copyright {
      border-top: 1px solid #222330;
    }
    &__textCopyright {
      border-top: 1px solid #222330;
      font-size: 12px;
      color: #CECECE;
      padding: 10px 0;
    }
  }
}
</style>