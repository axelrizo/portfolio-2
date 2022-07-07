<template lang="pug">
Section.projects
  SectionHeader(:info="{ title: 'Projects' }")

  .projects__frontend
    ProjectCard(
      :info="{ name: 'Devfest', description: 'We need for \"GDG México Unido\" a way to load the event page with information easier and I was assigned as the leader of 3 novice programmers to do it' }",
      :image="require('~/assets/image/project_GDG.png')",
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
