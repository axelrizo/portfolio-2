<template lang="pug">
header.header
  IconLogo.header__logo
  LayoutHeaderToggle.header__toggle(
    @click.native="toggleMenuShow()",
    :showMenu="showMenu"
  )
  transition(name="fade")
    LayoutHeaderNav(v-show="showMenu", @click.native="toggleMenuShow()")
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
      window.screen.width >= 1200
        ? (this.showMenu = true)
        : (this.showMenu = !this.showMenu);
    },
    onResize() {
      window.screen.width >= 1200
        ? (this.showMenu = true)
        : (this.showMenu = false);
      return this.showMenu;
    },
  },
  mounted() {
    if (process.browser) {
      this.onResize();
      addEventListener("resize", this.onResize);
    }
  },
};
</script>

<style lang="scss">
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
