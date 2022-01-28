<template lang="pug">
.hero.custom-container
  .hero__ava 
    Ava(:src="require('~/assets/img/ava_2020_tiny.jpeg')")
  .hero__text 
    h1.title-1 Hi, I am Kolin, #[br] Marketing Engineer
    .subtitle Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit. Exercitation veniam consequat sunt nostrud amet.
    .hero__actions
      b-button(type="is-danger") Download Resume
</template>

<script >
export default {};
</script>

<style lang="scss" >
.hero {
  @apply "py-12 sm:(flex py-16 flex-row-reverse) ";
  &__ava {
    @apply "sm:ml-14 flex justify-center";
  }
  &__text {
    @apply "<sm:text-center";
  }
  &__actions {
    @apply "mt-8";
  }
}
.ava {
}
</style>