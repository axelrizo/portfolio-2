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
@import "@/assets/css/_variables.scss";
.section-subtitle {
  font-size: 30px;
  color: #fff;
  padding: 50px 0;
  &::before {
    content: "> ";
    color: rgba(var(--color-principal));
  }
  @media (min-width: $md) {
    font-size: 40px;
  }
}
</style>