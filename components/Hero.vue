<template lang="pug">
.hero
  .hero__text
    h2.hero__title Hi, I'm Axel Rizo
    h1.hero__subtitle Self-taught web developer
  .hero__picture
    .hero__circle-gradient
    img.hero__image(src="~/assets/image/hero_axel_image.png", alt="altText")
</template>

<script>
export default {};
</script>

<style lang="scss">
.hero {
  height: 100vh;
  background-image: url("~/assets/image/hero_background_topography.svg");
  background-color: #000000;
  background-position: center;
  background-attachment: fixed;
  z-index: 100;
  position: relative;
  min-height: 568px;

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
  &__text {
    color: #fff;
    position: absolute;
    z-index: 300;
    top: 125px;
    left: 50%;
    transform: translateX(-50%);
    white-space: nowrap;
    display: flex;
    flex-direction: column;
    gap: 5px;
  }
  &__title {
    font-size: 35px;
  }
  &__subtitle {
    font-size: 15px;
  }
  &__picture {
    position: absolute;
    bottom: 0;
    right: -5px;
    z-index: 300;
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
  }
  &__image {
    position: relative;
    width: 192px;
    height: 342px;
  }
}
</style>