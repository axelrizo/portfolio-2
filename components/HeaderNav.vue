<template lang="pug">
nav.nav
  a.nav__link(href="#about", title="title") ABOUT
  a.nav__link(href="#projects", title="title") PROJECTS
  a.nav__link(href="#contact", title="title") CONTACT
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "~/assets/css/_variables.scss";
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
  font-size: 20px;
  @media (min-width: $md) {
    top: 100px;
    font-size: 30px;
    gap: 15px;
    padding: 50px 15px;
  }
  @media (min-width: $xl) {
    position: relative;
    flex-direction: row;
    border: initial;
    background-color: initial;
    padding: initial;
    top: initial;
    right: initial;
    font-size: 24px;
  }
  &__link {
    padding: 10px 20px;
    color: #fff;
    text-decoration: none;
    transition: color 0.5s;
  }
}
</style>