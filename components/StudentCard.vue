<template lang="pug">
a.student-card(:href="info.link", title="title", target="_blank")
  IconGithub.student-card__icon
  h4.student-card__name &lt;{{ info.name }}/&gt;
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

<style lang="scss" scoped>
.student-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
  text-decoration: none;
  &__icon {
    width: 100px;
    height: 100px;
    color: #fff;
  }
  &__name {
    font-size: 20px;
    color: rgba(var(--color-principal));
  }
}
</style>
