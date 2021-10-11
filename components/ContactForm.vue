<template lang="pug">
form.contact-form(action="", method="POST")
  textarea.contact-form__input.contact-form__input--textarea(
    required,
    placeholder="Write something..."
  )
  input.contact-form__input.contact-form__input--name(
    type="text",
    required,
    placeholder="Name"
  )
  input.contact-form__input.contact-form__input--email(
    type="email",
    required,
    placeholder="Email"
  )
  input.contact-form__input.contact-form__input--submit(
    type="submit",
    required,
    value="<Send/>"
  ) 
</template>

<script>
export default {};
</script>

<style lang="scss">
.contact-form {
  display: flex;
  flex-direction: column;
  gap: 10px;
  &__input {
    width: 100%;
    border: none;
    border-radius: 30px;
    background-color: #e5e5e5;
    color: #696969;
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