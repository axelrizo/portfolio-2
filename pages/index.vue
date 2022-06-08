<template lang="pug">
.app
  Header
  Hero
  About#about
  Projects#projects
  Contact#contact
</template>

<style lang="scss">
.app {
  --color-principal: 234, 76, 76;
  --color-secondary-1: 193, 69, 69;
  --color-secondary-2: 250, 244, 208;
  overflow-x: hidden;
  background-color: #000;
  position: relative;
  margin: auto;
  max-width: 1400px;
}

* {
  font-family: "Poppins", sans-serif;
  box-sizing: border-box;
}
</style>
