<template lang="pug">
Section.projects
  SectionHeader(:info="{ title: 'Projects' }") 

  SectionSubtitle(:info="{ subtitle: 'Frontend' }") 

  .projects__frontend
    FrontendCard(
      :info="{ name: 'Portfolio 2.0', description: 'I needed a new portfolio, one that I like it, then, with my new knowledge I did one, I use Nuxt as Static Site Generator and Vue' }",
      :image="require('~/assets/image/projects_1.png')",
      github="https://github.com/AxelRSa/portfolio-2",
      figma="https://www.figma.com/file/ReOLbiaCQ6sVNin62pd8n9/Portfolio-2.0?node-id=29%3A326"
    )
      TechContainer.frontend-card__tech(
        :technologies="{ Nuxt: true, Vue: true, Pug: true, Sass: true, Figma: true }"
      )

    FrontendCard(
      :info="{ name: 'Salón Rizo 2.0', description: 'There is the second version of a webpage that I realized, in the second version I use BEM CSS metodology and I tried to do components with Pug and Sass.' }",
      :image="require('~/assets/image/projects_2.png')",
      github="https://github.com/AxelRSa/salon-rizo",
      link="http://salonrizo.com/"
    )
      TechContainer.frontend-card__tech(
        :technologies="{ Pug: true, Sass: true, JavaScript: true, PHP: true, MySQL: true, Webpack: true }"
      )

    FrontendCard(
      :info="{ name: 'Portfolio 1.0', description: `This is one of my first projects, I don't do projects often because I like to learn a lot of things that could be better for the next one.` }",
      :image="require('~/assets/image/projects_3.png')",
      github="https://github.com/AxelRSa/portafolio-axel-rizo",
      link="https://axelrizo.tech/v1"
    )
      TechContainer.frontend-card__tech(
        :technologies="{ Pug: true, Sass: true, JavaScript: true }"
      )

  SectionSubtitle(:info="{ subtitle: 'Backend' }") 

  .projects__backend
    BackendCard(
      :info="{ name: 'Angeline Bags CRUD/API', description: `A only participate on the backend side making a CRUD that save information and save images to after create an API for the page AngelineBags` }",
      github="https://github.com/AxelRSa/portafolio-axel-rizo"
    )
    BackendCard(
      :info="{ name: 'Salon Rizo API', description: `I needed the information from instagram and I make it connect to my database using an` }",
      github="https://github.com/AxelRSa/portafolio-axel-rizo"
    )

  //- ProjectsBackend
</template>

<script>
export default {};
</script>

<style lang="scss">
.projects {
  &__frontend {
    display: flex;
    flex-direction: column;
    gap: 80px;
    padding: 20px 0 50px 0;
  }
  &__backend {
    display: flex;
    flex-direction: column;
    gap: 80px;
    padding: 20px 0 50px 0;
  }
}
</style>