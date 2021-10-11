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
  padding: 20px 0;
  @media (min-width: $md) {
    font-size: 40px;
  }
}
</style>