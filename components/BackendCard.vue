<template lang="pug">
.backend-card
  h3.backend-card__name {{ info.name }}
  slot
  p.backend-card__description {{ info.description }}
  .backend-card__container
    a.backend-card__link(
      v-if="github",
      :href="github",
      target="_blank",
      title="title"
    )
      IconGithub.backend-card__icon
      span.backend-card__text &lt;Github/&gt;
</template>
<script>
export default {
  props: {
    info: Object,
    github: String,
  },
};
</script>
<style lang="scss">
.backend-card {
  display: flex;
  flex-direction: column;
  gap: 20px;
  &__name {
    color: #fff;
    font-size: 20px;
  }
  &__tech {
    display: flex;
    gap: 5px;
    .tech__icon {
      height: 30px;
      width: 30px;
    }
  }
  &__description {
    color: #d2d2d2;
    line-height: 1.5;
    font-size: 16px;
  }
  &__container {
    display: flex;
    gap: 10px;
  }
  &__link {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    text-decoration: none;
  }
  &__icon {
    width: 30px;
    height: 30px;
    color: #fff;
  }
  &__text {
    color: rgba(var(--color-principal));
    font-size: 16px;
  }
}
</style>