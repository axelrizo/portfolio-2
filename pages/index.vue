<template lang="pug">
.index-page
  //- hero
  .hero
    .hero__text
      BaseText(tag="h1").text-35px.text-md-70px Hi, I'm Axel Rizo
      BaseText(tag="h2").text-15px.text-md-25px Self-taught frontend developer
    .hero__picture
      .hero__circle-gradient
      img.hero__image(src="~/assets/image/hero_axel_image.png", alt="altText")

  //- about
  BaseContainer.about
    SectionTitle.text-white About

    BaseText
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
      p.section-text__p I learn fast , I'm self taught and I'm an passionate of good code and simplicity.

    BaseSubtitle(:info="{ subtitle: 'Technologies' }")

    BaseTechContainer.about__tech(
      :technologies="{ Vue: true, Nuxt: true, Pug: true, Sass: true, Git: true, Bootstrap: true }"
    )

    BaseSubtitle(:info="{ subtitle: 'Community' }")

    BaseText
      p.section-text__p
        | One of my activities being mentored by&nbsp;
        a.section-text__link(
          href="https://www.youtube.com/c/Jos%C3%A9DimasLuj%C3%A1nCastillo",
          target="_blank",
          title="title"
        ) &lt;José Dimas/&gt;
        | &nbsp;is to teach and share my knowledge, I taught two programmers, and I’m currently teaching from scratch to:

    .about__students
      BaseStudentCard(
        :info="{ link: 'https://github.com/SA-Zenk', name: 'SA-Zenk' }"
      )

    BaseText
      p.section-text__p I like events and get involved:
      p.section-text__p In 2018 I was an espectator of Devfest Cancún 2018
      p.section-text__p In 2019 I was staff in Devfest Cancún 2019
      p.section-text__p I was participating with a Google community named "GDG Cancún", that organize DevFest, as presentator:

    .about__youtube
      BaseYoutubeIframe(
        :info="{ link: 'https://www.youtube.com/embed/RrRcC6ntRvk' }"
      )
      BaseYoutubeIframe(
        :info="{ link: 'https://www.youtube.com/embed/5P9_w4Yqjws' }"
      )

    BaseText
      p.section-text__p in 2021 I had a conference teaching how they can be a programmer without degree and I participate as presenter

    .about__youtube
      BaseYoutubeIframe(
        :info="{ link: 'https://www.youtube.com/embed/fO7tbEDrPxc' }"
      )
      BaseYoutubeIframe(
        :info="{ link: 'https://www.youtube.com/embed/t9V1zxXv4-k' }"
      )

    BaseText
      p.section-text__p
        | And developer, I worked on a platform copy of&nbsp;
        a.section-text__link(
          href="https://hoverboard-master.web.app/",
          target="_blank",
          title="title"
        ) &lt;Hoverboard/&gt;
        | &nbsp;by leading a group of 3 new developers.

  BaseContainer.projects
    SectionTitle Projects

    .projects__frontend
      ProjectCard(
        :info="{ name: 'Devfest', description: 'We need for \"GDG México Unido\" a way to load the event page with information easier and I was assigned as the leader of 3 novice programmers to do it' }",
        :image="require('~/assets/image/project_GDG.png')",
        link="https://devfestmexico.herokuapp.com",
        :frontend="true"
      )
        BaseTechContainer.project-card__tech(
          :technologies="{ Vue: true, Pug: true, Sass: true }"
        )
  BaseContainer.contact
    SectionTitle Contact
    p.contact__text Say hello! :)
    form.contact__form.contact-form(
      v-on:submit.prevent="onSubmit()",
      method="POST",
      ref="contactForm"
    )
      input.contact-form__input.contact-form__input--email(
        type="email",
        required,
        placeholder="Email",
        name="email",
        value="test@test"
      )
      input.contact-form__input.contact-form__input--name(
        type="text",
        required,
        placeholder="Name",
        name="name",
        value="test"
      )
      textarea.contact-form__input.contact-form__input--textarea(
        required,
        placeholder="Write something...",
        name="content"
      ) test
      input.contact-form__input.contact-form__input--submit(
        type="submit",
        required,
        value="<Send/>"
      )
</template>

<script>
export default {
  methods: {
    async onSubmit() {
      const form = this.$refs.contactForm;
      const url = "https://backend.axelrizo.tech/";
      const data = new FormData(form);
      const response = await fetch(url, {
        method: "POST",
        body: new URLSearchParams(data),
      });
      console.log(response);
    },
  },
};
</script>

<style lang="scss" scoped>
.hero {
  height: 100vh;
  background-image: url("~/assets/image/hero_background_topography.svg");
  background-color: #000000;
  background-position: center;
  background-attachment: fixed;
  z-index: 100;
  position: relative;
  min-height: 568px;

  @media (min-width: $md) {
    min-height: 670px;
  }

  &::before {
    content: "";
    background-color: #00000088;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 200;
  }
  &::after {
    content: "";
    @media (min-width: $xl) {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 201;
      background: linear-gradient(
        90deg,
        rgba(0, 0, 0, 1) 0%,
        rgba(0, 0, 0, 0) 10%,
        rgba(0, 0, 0, 0) 90%,
        rgba(0, 0, 0, 1) 100%
      );
    }
  }
  &__text {
    color: #fff;
    position: absolute;
    z-index: 300;
    top: 30%;
    left: 50%;
    transform: translateX(-50%);
    white-space: nowrap;
    display: flex;
    flex-direction: column;
    gap: 5px;
    @media (min-width: $md) {
      left: 10%;
      transform: translateX(0);
    }
    @media (min-width: $xl) {
      top: 50%;
      transform: translateY(-50%);
    }
  }

  &__picture {
    position: absolute;
    bottom: 0;
    right: -5px;
    z-index: 300;
    @media (min-width: $md) {
      right: -20px;
    }
    @media (min-width: $xl) {
      right: 10%;
      top: 50%;
      transform: translateY(-50%);
    }
  }
  &__circle-gradient {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    width: 315px;
    height: 315px;
    border-radius: 50%;
    background: linear-gradient(
      rgba(var(--color-secondary-1), 0.7),
      rgba(var(--color-secondary-2), 0.7)
    );
    @media (min-width: $md) {
      width: 392px;
      height: 392px;
    }
    @media (min-height: 900px) {
      height: 530px;
      width: 530px;
    }
  }
  &__image {
    position: relative;
    width: 192px;
    height: 342px;
    border-radius: 10px;
    @media (min-width: $md) {
      height: 426px;
      width: 239px;
    }
    @media (min-height: 900px) {
      height: 577px;
      width: 325px;
    }
  }
}

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

.contact {
  &__text {
    color: #fff;
    text-align: center;
    padding: 30px;
    font-size: 18px;
    @media (min-width: $md) {
      font-size: 20px;
    }
  }
}

.contact-form {
  display: flex;
  flex-direction: column;
  gap: 10px;
  @media (min-width: $md) {
    gap: 20px;
    width: 500px;
    margin: 0 auto;
  }
  &__input {
    width: 100%;
    border: none;
    border-radius: 30px;
    background-color: #e5e5e5;
    color: #000;
    font-size: 16px;

    &:focus-visible {
      outline: none;
    }
    &--name,
    &--email {
      height: 30px;
      padding: 0 15px;
    }
    &--textarea {
      resize: none;
      height: 200px;
      padding: 5px 15px;
      border-radius: 15px;
    }
    &--submit {
      border: none;
      font-size: 32px;
      color: #fff;
      background-color: rgba(var(--color-principal));
    }
  }
}
</style>
