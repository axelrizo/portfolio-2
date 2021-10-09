<template lang="pug">
.contact
  .contact__header
    h3.contact__title Contact
      a.contact__link-to-top(href="#", title="title")
        IconArrowToTop.contact__icon
  .contact__container
    a.contact__link(href="mailto:axelg.rizos@gmail.com", title="title") Send me an email!
</template>

<script>
export default {};
</script>

<style lang="scss">
.contact {
  &__header {
    position: relative;
    margin: 0 auto;
    width: fit-content;
  }
  &__title {
    font-size: 36px;
    color: #fff;
    padding: 0 0 30px 0;
  }
  &__link-to-top {
    position: absolute;
    right: -70px;
    top: 0;
  }
  &__icon {
    width: 35px;
    height: 35px;
    color: rgba(var(--color-principal));
  }
  &__container {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 400px;
  }
  &__link {
    color: #fff;
    text-decoration: none;
    padding: 10px 20px;
    border-radius: 20px;
    background-color: rgba(var(--color-principal));
    font-size: 20px;
    text-align: center;
  }
}
</style>