<template lang="pug">
Section.projects
  SectionHeader(:info="{ title: 'Projects' }")

  .projects__frontend
    ProjectCard(
      :info="{ name: 'Devfest', description: 'I needed a new portfolio, one that I like it, then, with my new knowledge I did one, I use Nuxt as Static Site Generator and Vue' }",
      :image="require('~/assets/image/projects_1.png')",
      link="https://devfestmexico.herokuapp.com"
      :frontend="true"
    )
      TechContainer.project-card__tech(
        :technologies="{ Vue: true, Pug: true, Sass: true}"
      )
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "@/assets/css/_variables.scss";
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
    @media (min-width: $md) {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(400px, 1fr));
      grid-gap: 50px;
    }
  }
}
</style>
