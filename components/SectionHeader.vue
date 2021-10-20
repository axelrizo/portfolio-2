<template lang="pug">
.section-header
  h3.section-header__title {{ info.title }}
  a.section-header__link(href="#", title="title")
    IconArrowToTop.section-header__icon
</template>

<script>
export default {
  props: {
    info: {
      type: Object,
    },
  },
};
</script>

<style lang="scss">
@import "@/assets/css/_variables.scss";
.section-header {
  position: relative;
  margin: 0 auto;
  width: fit-content;
  &__title {
    font-size: 36px;
    color: #fff;
    padding: 0 0 60px 0;
    @media (min-width: $md) {
      font-size: 48px;
    }
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