
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
.toggle {
  position: relative;
  width: 30px;
  height: 30px;
  &__icon {
    pointer-events: none;
    position: absolute;
    top: 0;
    left: 0;
    width: 30px;
    height: 30px;
    color: #fff;
  }
}
</style>