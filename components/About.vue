<template lang="pug">
Section.about
  SectionHeader(:info="{ title: 'About' }")

  SectionText
    p.section-text__p My journey began when I was in my career and I discovered from myself that I like the automatization of Excel, then, I began to learn to code in my career and I knew that it was for me and here we are.
    p.section-text__p I have a degree in Enterprise Innovation in "Universidad del Caribe" one of the best universities of Cancun.
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
    :technologies="{ Vue: true, Nuxt: true, Pug: true, Sass: true, Git: true, Bootstrap: true }"
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
      | &nbsp;is to teach and share my knowledge, I taught two programmers, and I’m currently teaching from scratch to:

  .about__students
    StudentCard(
      :info="{ link: 'https://github.com/SA-Zenk', name: 'SA-Zenk' }"
    )

  SectionText
    p.section-text__p I like events and get involved:
    p.section-text__p In 2018 I was an espectator of Devfest Cancún 2018
    p.section-text__p In 2019 I was staff in Devfest Cancún 2019
    p.section-text__p I was participating with a Google community named "GDG Cancún", that organize DevFest, as presentator:

  .about__youtube
    YoutubeIframe(
      :info="{ link: 'https://www.youtube.com/embed/RrRcC6ntRvk' }"
    )
    YoutubeIframe(
      :info="{ link: 'https://www.youtube.com/embed/5P9_w4Yqjws' }"
    )

  SectionText
    p.section-text__p in 2021 I had a conference teaching how they can be a programmer without degree and I participate as presenter

  .about__youtube
    YoutubeIframe(
      :info="{ link: 'https://www.youtube.com/embed/fO7tbEDrPxc' }"
    )
    YoutubeIframe(
      :info="{ link: 'https://www.youtube.com/embed/t9V1zxXv4-k' }"
    )

  SectionText
    p.section-text__p
      | And developer, I worked on a platform copy of&nbsp;
      a.section-text__link(
        href="https://hoverboard-master.web.app/",
        target="_blank",
        title="title"
      ) &lt;Hoverboard/&gt;
      | &nbsp;by leading a group of 3 new developers.
</template>

<script>
export default {};
</script>

<style lang="scss">
.about {
  &__tech {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(50px, 1fr));
    grid-gap: 20px;
    padding: 30px 0;
    @media (min-width: $md) {
      grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
      grid-gap: 35px 70px;
    }
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
    @media (min-width: $md) {
      flex-direction: row;
    }
  }
}
</style>
