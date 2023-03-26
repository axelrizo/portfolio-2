<template lang="pug">
.text(:is="tag", v-bind="$attrs")
  slot
</template>

<script>
export default {
  props: {
    tag: {
      type: String,
      default: "p",
    },
  },
};
</script>

<style lang="scss" scoped>
.text-15px {
  font-size: 15px;
}

.text-35px {
  font-size: 35px;
}

@media (min-width: $md) {
  .text-md{
    &-70px {
      font-size: 70px;
    }

    &-48px {
      font-size: 48px;
    }

    &-25px {
      font-size: 25px;
    }
  }
}

.text-color {

}
</style>
