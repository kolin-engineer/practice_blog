<template lang="pug">
section.recent-posts
  .custom-container
    .recent-posts__headline
      .title-section Recent Posts
      nuxt-link.recent-posts__action(to="") View all
    .recent-posts__cards
      PostCard
      PostCard
</template>


<style lang="scss" scoped>
.recent-posts {
  @apply "bg-blue-100 pb-8";
  &__headline {
    @apply "py-4 flex justify-between";
  }
  &__action {
  }
  &__cards {
    @apply "sm:flex";
  }
}
</style>