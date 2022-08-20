<template lang="pug">
h2.section-subtitle {{ info.subtitle }}
</template>

<script>
export default {
  props: {
    info: {
      type: Object,
    },
  },
};
</script>

<style lang="scss">

.section-subtitle {
  font-size: 30px;
  color: #fff;
  padding: 100px 0 40px;
  &::before {
    content: "> ";
    color: rgba(var(--color-principal));
  }
  @media (min-width: $md) {
    font-size: 40px;
  }
}
</style>
