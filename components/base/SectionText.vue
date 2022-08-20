<template lang="pug">
.section-text
  slot
</template>

<script>
export default {};
</script>

<style lang="scss">

.section-text {
  display: flex;
  flex-direction: column;
  gap: 55px;
  padding: 30px 0;

  &__p {
    color: #d2d2d2;
    line-height: 1.5;
    font-size: 18px;
    max-width: 80ch;
    @media (min-width: $md) {
      font-size: 20px;
    }
  }
  &__link {
    color: rgba(var(--color-principal));
    text-decoration: none;
  }
}
</style>
