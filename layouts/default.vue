<template lang="pug">
BaseContainer.layout-default.xxl
  LayoutHeaderMobile.layout-default__header-mobile
  LayoutHeaderDesktop.layout-default__header-desktop
  Nuxt
</template>

<style lang="scss" scoped>
.layout-default{
  position: relative;

  &__header-mobile {
    @media (min-width: $lg) {
      display: none;
    }
  }

  &__header-desktop {
    display: none;
    @media (min-width: $lg) {
      display: flex;
    }
  }
}
</style>
