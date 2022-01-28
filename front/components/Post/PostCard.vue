<script setup>
</script>
<template lang="pug">
.post-card(shadow="hover")
  .title-2 Making a design system from scratch
  .post-card__tags 12 Feb 2020 | Figma, Icon Design
  .post-card__text Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis, velit dolor eaque ipsa temporibus modi expedita laboriosam sequi cupiditate voluptates delectus optio rem eos ullam iste corrupti laudantium aliquam similique?
</template>
<style lang="scss">
.post-card {
  @apply "bg-white p-4 rounded-md border-gray-200 border-1 hover:(shadow-md cursor-pointer) transition-shadow duration-400";
  & + & {
    @apply "mt-4 sm:(mt-0 ml-4)";
  }
  &__tags {
    @apply "text-sm mt-4";
  }

  &__text {
    @apply "mt-4";
  }
}
</style>