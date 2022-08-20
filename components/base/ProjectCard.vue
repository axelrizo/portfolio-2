<template lang="pug">
.project-card(:class="{ 'project-card--frontend': frontend }")
  h3.project-card__name {{ info.name }}
  .project-card__container-data
    img.project-card__image(v-if="image", :src="image", alt="altText")
    .project-card__container-info
      p.project-card__description {{ info.description }}
      slot
      .project-card__container-link
        a.project-card__link(
          v-if="github",
          :href="github",
          target="_blank",
          title="title"
        )
          IconGithub.project-card__icon
          span.project-card__text &lt;Github/&gt;
        a.project-card__link(
          v-if="figma",
          :href="figma",
          target="_blank",
          title="title"
        )
          IconFigma.project-card__icon
          span.project-card__text &lt;Figma/&gt;
        a.project-card__link(
          v-if="link",
          :href="link",
          target="_blank",
          title="title"
        )
          IconLink.project-card__icon
          span.project-card__text &lt;Link/&gt;
</template>
<script>
export default {
  props: {
    info: Object,
    github: String,
    figma: String,
    link: String,
    image: String,
    frontend: Boolean,
  },
};
</script>
<style lang="scss">

.project-card {
  display: flex;
  flex-direction: column;
  gap: 20px;
  &--frontend {
    .project-card {
      &__container-data {
        @media (min-width: $lg) {
          flex-direction: row;
          gap: 50px;
        }
      }
      &__container-info {
        @media (min-width: $lg) {
          justify-content: space-between;
        }
      }
    }
  }
  &__container-data {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  &__image {
    height: 100%;
    width: 100%;
    @media (min-width: $lg) {
      width: 50%;
    }
  }

  &__container-info {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }
  &__name {
    color: #fff;
    font-size: 24px;
    @media (min-width: $md) {
      font-size: 34px;
    }
  }
  &__tech {
    display: flex;
    gap: 5px;
    .tech__icon {
      height: 40px;
      width: 40px;
      @media (min-width: $md) {
        height: 50px;
        width: 50px;
      }
    }
  }
  &__description {
    color: #d2d2d2;
    line-height: 1.5;
    font-size: 18px;
    @media (min-width: $md) {
      font-size: 20px;
    }
  }
  &__container-link {
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
    width: 40px;
    height: 40px;
    color: #fff;
    @media (min-width: $md) {
      height: 60px;
      width: 60px;
    }
  }
  &__text {
    color: rgba(var(--color-principal));
    font-size: 16px;
    @media (min-width: $md) {
      font-size: 22px;
    }
  }
}
</style>
