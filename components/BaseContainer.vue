<template lang="pug">
.container
  slot
</template>

<style lang="scss" scoped>
.container {
  margin: 0 auto;

  @media (min-width: $sm) {
    max-width: 516px;
  }

  @media (min-width: $md) {
    max-width: 668px;
  }

  @media (min-width: $lg) {
    max-width: 880px;
  }

  @media (min-width: $xl) {
    max-width: 1150px;
  }

  @media (min-width: $xxl) {
    max-width: 1350px;
  }
}

.xl {
  @media (min-width: $sm) {
    max-width: none;
  }

  @media (min-width: $md) {
    max-width: none;
  }

  @media (min-width: $lg) {
    max-width: none;
  }

  @media (min-width: $xl) {
    max-width: none;
  }

  @media (min-width: $xxl) {
    max-width: 1350px;
  }
}
</style>
