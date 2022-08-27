<template lang="pug">
.section-title
  BaseText(tag="h3").text-35px.text-md-48px
    slot
  a.section-title__link(href="#")
    IconArrowToTop.section-title__icon
</template>

<style lang="scss" scoped>
.section-title {
  position: relative;
  margin: 0 auto;
  width: fit-content;

  &__title {
    color: #fff;
    padding: 0 0 60px 0;
  }

  &__link {
    position: absolute;
    right: -60px;
    top: 0;
  }

  &__icon {
    width: 35px;
    height: 35px;
    color: rgba(var(--color-principal));

    @media (min-width: $md) {
      width: 48px;
      height: 48px;
    }
  }
}
</style>
