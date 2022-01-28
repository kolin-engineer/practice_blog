<template lang="pug">
.work-card 
  .work-card__img
    b-image.rounded-sm(src="http://unsplash.it/600/600?random&gravity=center")
  .work-card__text
    .title-2 Designing Dashboards
    .work-card__tags 
      b-tag 2021
      span.ml-4 Dashboard
    .work-card__preview Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit. Exercitation veniam consequat sunt nostrud amet.
</template>

<script>
export default {};
</script>


<style lang="scss" scoped>
.work-card {
  @apply "sm:(flex py-5) border-b-light-800 border-b-1";
  & + & {
    @apply "mt-4";
  }
  &__img {
    @apply "sm:max-w-50 overflow-hidden";
  }
  &__text {
    @apply "sm:ml-4";
  }
  &__tags {
    @apply "mt-4 font-thin";
  }
  &__preview {
    @apply "mt-4";
  }
}
</style>