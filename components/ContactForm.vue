<template lang="pug">
form.contact-form(v-on:submit.prevent="onSubmit()", method="POST", ref="contactForm")
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
        body: new URLSearchParams((data)),
      });
      console.log(response);
    },
  },
};
</script>

<style lang="scss">

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
