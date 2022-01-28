<template lang="pug">
.ava
  .ava__deco
  .ava__img
    b-image(:src="src")
</template>

<script>
export default {
  props: {
    src: String,
  },
  setup(props) {},
};
</script>



<style lang="scss" scoped>
.ava {
  @apply "relative inline-flex justify-center";
  &__img,
  &__deco {
    @apply "w-180px h-180px md:(w-240px h-240px) rounded-1/2 overflow-hidden border-none ";
  }
  &__deco {
    content: "";
    background-color: #edf7fa;
    @apply "absolute rounded-1/2 block top-13px ";
    left: -5px;
  }
}
</style>