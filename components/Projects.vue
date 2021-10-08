<template lang="pug">
.projects
  .projects__header
    h3.projects__title Projects
      a.projects__link-to-top(href="#", title="title")
        IconArrowToTop.projects__icon
  .projects__subtitle Frontend
  ProjectsFrontend
  .projects__subtitle Backend
  ProjectsBackend
</template>

<script>
export default {};
</script>

<style lang="scss">
.projects {
  padding: 40px 15px;
  &__header {
    position: relative;
    margin: 0 auto;
    width: fit-content;
  }
  &__title {
    font-size: 36px;
    color: #fff;
    padding: 0 0 30px 0;
  }
  &__link-to-top {
    position: absolute;
    right: -70px;
    top: 0;
  }
  &__icon {
    width: 35px;
    height: 35px;
    color: rgba(var(--color-principal));
  }
  &__subtitle {
    font-size: 28px;
    color: #fff;
    padding: 20px 0;
  }
}
</style>