<template lang="pug">
.section
  slot
</template>
<style lang="scss">
@import "@/assets/css/_variables.scss";
.section {
  @media (min-width: $sm) {
    margin: 0 auto;
    max-width: 516px;
  }
  @media (min-width: $md) {
    max-width: 668px;
  }
  padding: 40px 15px;
}
</style>