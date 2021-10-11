<template lang="pug">
iframe.youtube-iframe(
  :src="info.link",
  title="YouTube video player",
  frameborder="0",
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture",
  allowfullscreen
)
</template>

<script>
export default {
  props: {
    info: {
      type: Object,
    },
  },
};
</script>

<style lang="scss">
.youtube-iframe {
  width: 100%;
  height: 100%;
  max-width: 320px;
}
</style>