<template lang="pug">
.frontend-card
  h3.frontend-card__name {{ info.name }}
  img.frontend-card__image(:src="image", alt="altText")
  slot
  p.frontend-card__description {{ info.description }}
  .frontend-card__container
    a.frontend-card__link(
      v-if="github",
      :href="github",
      target="_blank",
      title="title"
    )
      IconGithub.frontend-card__icon
      span.frontend-card__text &lt;Github/&gt;
    a.frontend-card__link(
      v-if="figma",
      :href="figma",
      target="_blank",
      title="title"
    )
      IconFigma.frontend-card__icon
      span.frontend-card__text &lt;Figma/&gt;
    a.frontend-card__link(
      v-if="link",
      :href="link",
      target="_blank",
      title="title"
    )
      IconLink.frontend-card__icon
      span.frontend-card__text &lt;Link/&gt;
</template>
<script>
export default {
  props: {
    info: Object,
    github: String,
    figma: String,
    link: String,
    image: String,
  },
};
</script>
<style lang="scss">
.frontend-card {
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