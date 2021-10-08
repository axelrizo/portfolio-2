<template lang="pug">
.about
  .about__header
    h3.about__title About
    a.about__link-to-top(href="#", title="title")
      IconArrowToTop.about__icon
  .about__text-container
    p.about__p My journey began when I was in my career and I discovered from myself that I like the automatization of Excel, then, I began to learn to code in my career and I knew that it was for me and here we are.
    p.about__p I have a degree in Enterprise Innovation in Universidad del Caribe one of the best universities of Cancun.
    p.about__p I began to study programming with <a class="about__link" href="https://www.youtube.com/c/Jos%C3%A9DimasLuj%C3%A1nCastillo" target="_blank" title="title">&lt;José Dimas/&gt;</a>, that has a Youtube Channel and is a teacher in my university.
    p.about__p I learn fast , I'm self taught and I'm an apasionate of good code and simplicity.
  .about__subtitle Tecnologies
  TechContainer.about__tech(
    :tecnologies="{ HTML: true, CSS: true, JavaScript: true, Vue: true, Nuxt: true, Pug: true, Sass: true, Git: true, PHP: true, MySQL: true, Bootstrap: true, Webpack: true, Figma: true }"
  )
  .about__subtitle Community
  .about__text-container
    p.about__p One of my activities being mentored by <a class="about__link" href="https://www.youtube.com/c/Jos%C3%A9DimasLuj%C3%A1nCastillo" target="_blank" title="title">&lt;José Dimas/&gt;</a> is to teach and share my knowledge, and I’m currently teaching two persons from scratch:
  .students-block
    a.students-block__student(
      href="https://github.com/microazteca",
      title="title",
      target="_blank"
    )
      IconGithub.students-block__github
      h4.students-block__name &lt;microazteca/&gt;
    a.students-block__student(
      href="https://github.com/SA-Zenk",
      title="title",
      target="_blank"
    )
      IconGithub.students-block__github
      h4.students-block__name &lt;SA-Zenk/&gt;
  .about__text-container
    p.about__p I like events and get involved:
    p.about__p In 2018 I was an espectator of Devfest Cancún 2018
    p.about__p In 2019 I was staff in Devfest Cancún 2019
    p.about__p I’m currently participating with a Google community named GDG Cancún, that organize DevFest, as presentator:
  .youtube
    iframe.youtube__iframe(
      src="https://www.youtube.com/embed/RrRcC6ntRvk",
      title="YouTube video player",
      frameborder="0",
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture",
      allowfullscreen
    )
    iframe.youtube__iframe(
      src="https://www.youtube.com/embed/5P9_w4Yqjws",
      title="YouTube video player",
      frameborder="0",
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture",
      allowfullscreen
    )
  .about__text-container
    p.about__p And developer, now I’m working on a platform copy of <a class="about__link" href="https://devfestmexico.com/" target="_blank" title="title">&lt;DevFest México/&gt;</a> by leading a group of developers. The reason of the project is that we are looking for flexibility because the original page was created with Hoverboard and it makes hard to change things.
</template>

<script>
export default {};
</script>

<style lang="scss">
.about {
  padding: 40px 15px;
  &__header {
    position: relative;
    margin: 0 auto;
    width: fit-content;
  }
  &__title {
    font-size: 36px;
    color: #fff;
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
  &__text-container {
    display: flex;
    flex-direction: column;
    padding: 30px 0;
    gap: 20px;
  }
  &__p {
    color: #d2d2d2;
    line-height: 1.5;
    font-size: 20px;
  }
  &__link {
    color: rgba(var(--color-principal));
    text-decoration: none;
  }
  &__subtitle {
    font-size: 28px;
    color: #fff;
    padding: 20px 0;
  }
  &__tech {
    padding: 20px 0;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-gap: 20px;
  }
}
.students-block {
  display: flex;
  gap: 10px;
  &__student {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    text-decoration: none;
  }
  &__github {
    width: 100px;
    height: 100px;
    color: #fff;
  }
  &__name {
    font-size: 20px;
    color: rgba(var(--color-principal));
  }
}
.youtube {
  display: flex;
  flex-direction: column;
  gap: 20px;
  &__iframe {
    width: 100%;
  }
}
</style>