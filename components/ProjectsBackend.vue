<template lang="pug">
.projects-backend
  .project
    h3.project__name Angeline Bags CRUD/API
    TechContainer.project__tech(
      :tecnologies="{ PHP: true, Bootstrap: true, MySQL: true }"
    )
    p.project__p A only participate on the backend side making a CRUD that save information and save images to after create an API for the page AngelineBags
    .project__links-container
      a.project__link(
        href="https://github.com/AxelRSa/portafolio-axel-rizo",
        target="_blank",
        title="title"
      )
        IconGithub.project__icon
        span.project__text &lt;Github/&gt;
  .project
    h3.project__name Salon Rizo API
    TechContainer.project__tech(:tecnologies="{ PHP: true, MySQL: true }")
    p.project__p I needed the information from instagram and I make it connect to my database using an
    .project__links-container
      a.project__link(
        href="https://github.com/AxelRSa/portafolio-axel-rizo",
        target="_blank",
        title="title"
      )
        IconGithub.project__icon
        span.project__text &lt;Github/&gt;
</template>

<script>
export default {};
</script>

<style lang="scss" >
.projects-backend {
  display: flex;
  flex-direction: column;
  gap: 70px;
  padding: 0 0 50px 0;
  .project {
    display: flex;
    flex-direction: column;
    gap: 10px;
    &__name {
      color: #fff;
      font-size: 20px;
      line-height: 1.3;
    }
    &__tech {
      display: flex;
      gap: 5px;
      .tech__icon {
        height: 30px;
        width: 30px;
      }
    }
    &__p {
      color: #d2d2d2;
      line-height: 1.5;
      font-size: 16px;
    }
    &__links-container {
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
}
</style>