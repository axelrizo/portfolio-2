<template lang="pug">
.hero
  .hero__text
    h2.hero__title Hi, I'm Axel Rizo
    h1.hero__subtitle Self-taught frontend developer
  .hero__picture
    .hero__circle-gradient
    img.hero__image(src="~/assets/image/hero_axel_image.png", alt="altText")
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "~/assets/css/_variables.scss";
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
  &__title {
    font-size: 35px;
    @media (min-width: $md) {
      font-size: 70px;
    }
  }
  &__subtitle {
    font-size: 15px;
    @media (min-width: $md) {
      font-size: 25px;
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
</style>