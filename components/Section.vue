<template lang="pug">
.section
  slot
</template>
<style lang="scss">

.section {
  padding: 150px 15px;
  @media (min-width: $sm) {
    margin: 0 auto;
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
</style>
