<template lang="pug">
header.header
  IconLogo.header__logo
  .toggle(@click="toggleMenuShow()")
    transition(name="fade")
      IconMenu.toggle__icon.toggle__icon--menu(v-show="!showMenu")
    transition(name="fade")
      IconClose.toggle__icon.toggle__icon--close(v-show="showMenu")
  transition(name="fade")
    nav.nav(v-show="showMenu", @click="toggleMenuShow()")
      a.nav__link(href="#about", title="title") ABOUT
      a.nav__link(href="#projects", title="title") PROJECTS
      a.nav__link(href="#contact", title="title") CONTACT
</template>

<script>
export default {
  data() {
    return {
      showMenu: false,
    };
  },
  methods: {
    toggleMenuShow(el) {
      this.showMenu = !this.showMenu;
      console.log(el);
    },
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

  &__logo {
    width: 198px;
    height: 30px;
    color: rgba(var(--color-principal));
  }
}
.toggle {
  position: relative;
  width: 30px;
  height: 30px;
  &__icon {
    position: absolute;
    top: 0;
    left: 0;
    width: 30px;
    height: 30px;
    color: #fff;
  }
}
.nav {
  position: absolute;
  top: 60px;
  right: 15px;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  background-color: #000;
  border-radius: 30px;
  padding: 30px 10px;
  border: 2px solid #fff;
  gap: 5px;
  &__link {
    padding: 10px 20px;
    color: #fff;
    text-decoration: none;
    transition: color 0.5s;
    &:hover {
      color: rgba(var(--color-principal));
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