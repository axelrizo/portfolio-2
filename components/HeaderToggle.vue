
<template lang="pug">
.toggle
  transition(name="fade")
    IconMenu.toggle__icon.toggle__icon--menu(v-show="!showMenu")
  transition(name="fade")
    IconClose.toggle__icon.toggle__icon--close(v-show="showMenu")
</template>

<script>
export default {
  props: {
    showMenu: Boolean,
  },
};
</script>

<style lang="scss">
@import "~/assets/css/_variables.scss";
.toggle {
  position: relative;
  width: 30px;
  height: 30px;
  @media (min-width: $md) {
    width: 50px;
    height: 50px;
  }
  &__icon {
    pointer-events: none;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    color: #fff;
  }
}
</style>