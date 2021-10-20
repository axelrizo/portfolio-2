<template lang="pug">
header.header
  IconLogo.header__logo
  HeaderToggle.header__toggle(
    @click.native="toggleMenuShow()",
    :showMenu="showMenu"
  )
  transition(name="fade")
    HeaderNav(v-show="showMenu", @click.native="toggleMenuShow()")
</template>

<script>
export default {
  data() {
    return {
      showMenu: this.onResize(),
    };
  },
  methods: {
    toggleMenuShow() {
      screen.width >= 1200
        ? (this.showMenu = true)
        : (this.showMenu = !this.showMenu);
    },
    onResize() {
      screen.width >= 1200 ? (this.showMenu = true) : (this.showMenu = false);
      return this.showMenu;
    },
  },
  mounted() {
    this.onResize();
    addEventListener("resize", this.onResize);
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
  @media (min-width: $md) {
    padding: 30px;
  }
  @media (min-width: $xl) {
    padding: 15px;
  }
  &__logo {
    width: 198px;
    height: 30px;
    color: rgba(var(--color-principal));
    @media (min-width: $md) {
      width: 290px;
      height: 44.5px;
    }
  }
  &__toggle {
    @media (min-width: $xl) {
      display: none;
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