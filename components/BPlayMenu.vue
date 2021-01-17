<template>
  <div>
    <ul class="menu">
      <li class="menu__item">ABOUT US</li>
      <li class="menu__item">PRODUCTS</li>
      <li class="menu__item">PARTNERS</li>
      <li class="menu__item">OUR CLIENTS</li>
      <li class="menu__item">CONTACT US</li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
.menu {
  display: flex;
  color: #FFF;
  list-style-type: none;

  &__item {
    padding: 10px 0;
    font-weight: bold;
    font-size: 16px;
    margin-left: 53px;

    &:first-child {
      border-bottom: 2px solid #F41616;
      margin-left: 0;
    }
  }
}

@media only screen and (max-width: 480px) and (min-width: 320px){
  .menu{
    display: none;
  }
}
</style>