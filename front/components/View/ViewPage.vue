<template lang="pug">
.page.custom-container
  .page__title
    slot(name="title")
  .page__content
    slot
</template>
  

<script>
export default {};
</script>

<style lang="scss">
.page {
  @apply "py-10";
  &__title {
    @apply "text-4xl font-semibold uppercase";
  }
}
</style>