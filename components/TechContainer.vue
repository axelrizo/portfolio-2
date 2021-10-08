<template lang="pug">
.tech
  IconHTML.tech__icon.tech__icon--HTML(v-if="tecnologies.HTML")
  IconCSS.tech__icon.tech__icon--CSS(v-if="tecnologies.CSS")
  IconJavaScript.tech__icon.tech__icon--JavaScript(
    v-if="tecnologies.JavaScript"
  )
  IconVue.tech__icon.tech__icon--Vue(v-if="tecnologies.Vue")
  IconNuxt.tech__icon.tech__icon--Nuxt(v-if="tecnologies.Nuxt")
  IconPug.tech__icon.tech__icon--Pug(v-if="tecnologies.Pug")
  IconSass.tech__icon.tech__icon--Sass(v-if="tecnologies.Sass")
  IconGit.tech__icon.tech__icon--Git(v-if="tecnologies.Git")
  IconPHP.tech__icon.tech__icon--PHP(v-if="tecnologies.PHP")
  IconMySQL.tech__icon.tech__icon--MySQL(v-if="tecnologies.MySQL")
  IconBootstrap.tech__icon.tech__icon--Bootstrap(v-if="tecnologies.Bootstrap")
  IconWebpack.tech__icon.tech__icon--Webpack(v-if="tecnologies.Webpack")
  IconFigma.tech__icon.tech__icon--Figma(v-if="tecnologies.Figma")
</template>

<script>
export default {
  props: ["tecnologies"],
};
</script>

<style lang="scss">
.tech {
  &__icon {
    color: white;
    &--HTML {
      color: #e34f26;
    }
    &--CSS {
      color: #1572b6;
    }
    &--JavaScript {
      color: #f7df1e;
    }
    &--Vue {
      color: #4fc08d;
    }
    &--Nuxt {
      color: #00dc82;
    }
    &--Pug {
      color: #a86454;
    }
    &--Sass {
      color: #cc6699;
    }
    &--Git {
      color: #f05032;
    }
    &--PHP {
      color: #777bb4;
    }
    &--MySQL {
      color: #4479a1;
    }
    &--Bootstrap {
      color: #7952b3;
    }
    &--Webpack {
      color: #8dd6f9;
    }
    &--Figma {
      color: #f24e1e;
    }
  }
}
</style>