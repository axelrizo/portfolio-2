<template lang="pug">
.app
  Header
  Hero
  About#about
  Projects#projects
  Contact#contact
  //- AppInstall(v-if="showInstall", style="background: white") Descargar APP
</template>

<script>
export default {
  // data() {
  //   return {
  //     showInstall: false,
  //   };
  // },
  mounted() {
    // // Initialize deferredPrompt for use later to show browser install prompt.
    // let deferredPrompt;
    // window.addEventListener("beforeinstallprompt", (e) => {
    //   // Prevent the mini-infobar from appearing on mobile
    //   e.preventDefault();
    //   // Stash the event so it can be triggered later.
    //   deferredPrompt = e;
    //   // Update UI notify the user they can install the PWA
    //   showInstallPromotion();
    //   // Optionally, send analytics event that PWA install promo was shown.
    //   console.log(`'beforeinstallprompt' event was fired.`);
    // });
  },
};
</script>

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
