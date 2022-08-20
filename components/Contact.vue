<template lang="pug">
Section.contact
  SectionHeader(:info="{ title: 'Contact' }")
  p.contact__text Say hello! :)
  ContactForm.contact__form
</template>

<script>
export default {};
</script>

<style lang="scss">
.contact {
  &__text {
    color: #fff;
    text-align: center;
    padding: 30px;
    font-size: 18px;
    @media (min-width: $md) {
      font-size: 20px;
    }
  }
}
</style>
