
<template lang="pug">
.toggle
  IconMenu.toggle__icon(v-if="!showMenu")
  IconClose.toggle__icon(v-else)
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
