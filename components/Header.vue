<template lang="pug">
header.header
  IconLogo.header__logo
  HeaderToggle(@click.native="toggleMenuShow()", :showMenu="showMenu")
  transition(name="fade")
    HeaderNav(v-show="showMenu", @click.native="toggleMenuShow()")
</template>

<script>
export default {
  data() {
    return {
      showMenu: false,
    };
  },
  methods: {
    toggleMenuShow() {
      this.showMenu = !this.showMenu;
    },
  },
};
</script>

<style lang="scss">
@import "~/assets/css/_variables.scss";
.header {
  z-index: 400;
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  display: flex;
  justify-content: space-between;
  padding: 15px;

  &__logo {
    width: 198px;
    height: 30px;
    color: rgba(var(--color-principal));
    @media (min-width: $md) {
      width: 290px;
      height: 44.5px;
    }
  }
}

.fade-enter {
  opacity: 0;
  transform: translateX(15px);

  &-active {
    transition: opacity 0.3s, transform 0.3s;
  }
  &-to {
    opacity: 1;
    transform: translateX(0px);
  }
}

.fade-leave {
  opacity: 1;
  transform: translateX(0px);

  &-active {
    transition: opacity 0.3s, transform 0.3s;
  }
  &-to {
    opacity: 0;
    transform: translateX(15px);
  }
}
</style>