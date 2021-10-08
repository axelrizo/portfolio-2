<template lang="pug">
.projects-frontend
  .project
    img.project__image(src="~/assets/image/projects_1.png", alt="altText")
    h3.project__name Portafolio 2.0
    TechContainer.project__tech(
      :tecnologies="{ Nuxt: true, Vue: true, Pug: true, Sass: true, Figma: true }"
    )
    p.project__p I needed a new portfolio, one that I like it, then, with my new knowledge I did one, I use Nuxt as Static Site Generator and Vue.
    .project__links-container
      a.project__link(
        href="https://github.com/AxelRSa/portfolio-2",
        target="_blank",
        title="title"
      )
        IconGithub.project__icon
        span.project__text &lt;Github/&gt;
      a.project__link(
        href="https://www.figma.com/file/ReOLbiaCQ6sVNin62pd8n9/Portfolio-2.0?node-id=29%3A326",
        target="_blank",
        title="title"
      )
        IconFigma.project__icon
        span.project__text &lt;Figma/&gt;
  .project
    img.project__image(src="~/assets/image/projects_2.png", alt="altText")
    h3.project__name Salón Rizo 2.0
    TechContainer.project__tech(
      :tecnologies="{ Pug: true, Sass: true, JavaScript: true, PHP: true, MySQL: true, Webpack: true }"
    )
    p.project__p There is the second version of a webpage that I realized, in the second version I use BEM CSS metodology and I tried to do components with Pug and Sass.
    .project__links-container
      a.project__link(
        href="https://github.com/AxelRSa/salon-rizo",
        target="_blank",
        title="title"
      )
        IconGithub.project__icon
        span.project__text &lt;Github/&gt;
      a.project__link(
        href="https://salonrizo.com/",
        target="_blank",
        title="title"
      )
        IconLink.project__icon
        span.project__text &lt;Link/&gt;
  .project
    img.project__image(src="~/assets/image/projects_3.png", alt="altText")
    h3.project__name Portfolio 1.0
    TechContainer.project__tech(
      :tecnologies="{ Pug: true, Sass: true, JavaScript: true }"
    )
    p.project__p This is one of my first projects, I don't do projects often because I like to learn a lot of things that could be better for the next one.
    .project__links-container
      a.project__link(
        href="https://github.com/AxelRSa/portafolio-axel-rizo",
        target="_blank",
        title="title"
      )
        IconGithub.project__icon
        span.project__text &lt;Github/&gt;
      a.project__link(
        href="http://axelrizo.tech/v1",
        target="_blank",
        title="title"
      )
        IconLink.project__icon
        span.project__text &lt;Link/&gt;
</template>

<script>
export default {};
</script>

<style lang="scss" >
.projects-frontend {
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