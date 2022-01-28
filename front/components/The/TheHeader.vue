<template lang="pug">
header.header
  .custom-container
    nav-bar
      template(#brand)
        nav-item 
          nuxt-link(to="/")
            b-image.logo(:src="require('~/assets/img/engineer_logo.png')")
      template(#start)
        nav-item
          nuxt-link(to="/blog") Blog
      template(#end)
        nav-item
          .buttons
            b-button(tag="a", to="", type="is-success") Login
            b-button(tag="a", to="") Sign Up
</template>

<style lang="scss" scoped>
.header {
  @apply " shadow-sm";
}
.logo {
  @apply "w-130px";
}
.nav {
  @apply "flex justify-end";

  &__item {
    & + & {
      @apply "ml-4";
    }
  }
}
</style>
