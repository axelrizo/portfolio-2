<template lang="pug">
Section.about
  SectionHeader(:info="{ title: 'About' }")

  SectionText
    p.section-text__p My journey began when I was in my career and I discovered from myself that I like the automatization of Excel, then, I began to learn to code in my career and I knew that it was for me and here we are.
    p.section-text__p I have a degree in Enterprise Innovation in Universidad del Caribe one of the best universities of Cancun.
    p.section-text__p 
      | I began to study programming with&nbsp;
      a.section-text__link(
        href="https://www.youtube.com/c/Jos%C3%A9DimasLuj%C3%A1nCastillo",
        target="_blank",
        title="title"
      ) &lt; José Dimas/ &gt;
      | , that has a Youtube Channel and is a teacher in my university.
    p.section-text__p I learn fast , I'm self taught and I'm an apasionate of good code and simplicity.

  SectionSubtitle(:info="{ subtitle: 'Tecnologies' }")

  TechContainer.about__tech(
    :technologies="{ HTML: true, CSS: true, JavaScript: true, Vue: true, Nuxt: true, Pug: true, Sass: true, Git: true, PHP: true, MySQL: true, Bootstrap: true, Webpack: true, Figma: true }"
  )

  SectionSubtitle(:info="{ subtitle: 'Community' }")

  SectionText
    p.section-text__p 
      | One of my activities being mentored by&nbsp;
      a.section-text__link(
        href="https://www.youtube.com/c/Jos%C3%A9DimasLuj%C3%A1nCastillo",
        target="_blank",
        title="title"
      ) &lt;José Dimas/&gt;
      | &nbsp;is to teach and share my knowledge, and I’m currently teaching two persons from scratch:

  .about__students
    StudentCard(
      :info="{ link: 'https://github.com/microazteca', name: 'microazteca' }"
    )
    StudentCard(
      :info="{ link: 'https://github.com/SA-Zenk', name: 'SA-Zenk' }"
    )

  SectionText
    p.section-text__p I like events and get involved:
    p.section-text__p In 2018 I was an espectator of Devfest Cancún 2018
    p.section-text__p In 2019 I was staff in Devfest Cancún 2019
    p.section-text__p I’m currently participating with a Google community named GDG Cancún, that organize DevFest, as presentator:

  .about__youtube
    YoutubeIframe(
      :info="{ link: 'https://www.youtube.com/embed/RrRcC6ntRvk' }"
    )
    YoutubeIframe(
      :info="{ link: 'https://www.youtube.com/embed/5P9_w4Yqjws' }"
    )

  SectionText
    p.section-text__p 
      | And developer, now I’m working on a platform copy of&nbsp;
      a.section-text__link(
        href="https://devfestmexico.com/",
        target="_blank",
        title="title"
      ) &lt;DevFest México/&gt;
      | &nbsp;by leading a group of developers. The reason of the project is that we are looking for flexibility because the original page was created with Hoverboard and it makes hard to change things.
</template>

<script>
export default {};
</script>

<style lang="scss">
.about {
  &__tech {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-gap: 20px;
  }
  &__students {
    display: flex;
    gap: 10px;
    padding: 20px 0;
  }
  &__youtube {
    display: flex;
    flex-direction: column;
    gap: 20px;
    padding: 20px 0;
  }
}
</style>