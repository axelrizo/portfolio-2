<template lang="pug">
.app
  Header
  Hero
  About#about
</template>

<script>
export default {};
</script>

<style lang="scss">
$sm: 576px;
$md: 768px;
$lg: 992px;
$xl: 1200px;
$xxl: 1400px;

.app {
  --color-principal: 234, 76, 76;
  --color-secondary-1: 193, 69, 69;
  --color-secondary-2: 250, 244, 208;
  overflow-x: hidden;
  background-color: #000;
}

* {
  font-family: "Poppins", sans-serif;
  box-sizing: border-box;
}
</style>