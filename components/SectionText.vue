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
  gap: 20px;
  &__p {
    color: #d2d2d2;
    line-height: 1.5;
    font-size: 16px;
  }
  &__link {
    color: rgba(var(--color-principal));
    text-decoration: none;
  }
}
</style>