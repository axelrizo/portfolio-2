<template lang="pug">
Section.contact
  SectionHeader(:info="{ title: 'Contact' }")
  .contact__container
    a.contact__link(href="mailto:axelg.rizos@gmail.com", title="title") Send me an email!
</template>

<script>
export default {};
</script>

<style lang="scss">
.contact {
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