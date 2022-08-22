<template lang="pug">
BaseContainer.contact
  BaseHeader(:info="{ title: 'Contact' }")
  p.contact__text Say hello! :)
  PageIndexContactForm.contact__form
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
