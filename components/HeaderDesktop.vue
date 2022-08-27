<template lang="pug">
BaseContainer.header.xxl
  IconLogo.header__logo
  nav.nav
    a.nav__link(href="#about") ABOUT
    a.nav__link(href="#projects") PROJECTS
    a.nav__link(href="#contact") CONTACT
</template>

<style lang="scss">
.header {
  z-index: var(--header);
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
</style>
