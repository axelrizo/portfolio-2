<template lang="pug">
.tech
  IconHTML.tech__icon.tech__icon--HTML(v-if="technologies.HTML")
  IconCSS.tech__icon.tech__icon--CSS(v-if="technologies.CSS")
  IconJavaScript.tech__icon.tech__icon--JavaScript(
    v-if="technologies.JavaScript"
  )
  IconVue.tech__icon.tech__icon--Vue(v-if="technologies.Vue")
  IconNuxt.tech__icon.tech__icon--Nuxt(v-if="technologies.Nuxt")
  IconPug.tech__icon.tech__icon--Pug(v-if="technologies.Pug")
  IconSass.tech__icon.tech__icon--Sass(v-if="technologies.Sass")
  IconGit.tech__icon.tech__icon--Git(v-if="technologies.Git")
  IconPHP.tech__icon.tech__icon--PHP(v-if="technologies.PHP")
  IconMySQL.tech__icon.tech__icon--MySQL(v-if="technologies.MySQL")
  IconBootstrap.tech__icon.tech__icon--Bootstrap(v-if="technologies.Bootstrap")
  IconWebpack.tech__icon.tech__icon--Webpack(v-if="technologies.Webpack")
  IconFigma.tech__icon.tech__icon--Figma(v-if="technologies.Figma")
</template>

<script>
export default {
  props: ["technologies"],
};
</script>

<style lang="scss" scoped>
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
