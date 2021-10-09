<template lang="pug">
.section-subtitle {{ info.subtitle }}
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
  font-size: 28px;
  color: #fff;
  padding: 20px 0;
}
</style>