<template lang="pug">
nav.nav
  .nav__brand(@click="close")
    slot(name="brand") 

  .nav__items(:class="{ 'nav__items--opened': opened }", @click="close")
    .nav__items-start
      slot(name="start")

    .nav__items-end
      slot(name="end")

  .nav__trigger
    .nav__item(@click="toggle")
      b-icon(:icon="opened ? 'close' : 'menu'", size="")
</template>

<script>
import { ref, onMounted } from "@nuxtjs/composition-api";
export default {
  setup(props) {
    const opened = ref(false);
    const toggle = function () {
      opened.value = !opened.value;
    };
    const close = function () {
      opened.value = false;
    };
    return { opened, toggle, close };
  },
};
</script>

<style lang="scss" scoped>
.nav {
  @apply "relative flex <sm:flex-col" sm:items-center;
  &__items {
    @apply "flex flex-1 justify-between <sm:hidden";
  }
  &__items--opened {
    @apply "<sm:(flex flex-col) border-t-1 border-t-light-300";
  }
  &__items-start {
    @apply "flex <sm:flex-col sm:items-center";
  }
  &__items-end {
    @apply "flex justify-end <sm:flex-col sm:items-center";
  }
  &__trigger {
    @apply "absolute";
  }
  &__item {
    @apply "block px-4 py-2 cursor-pointer select-none leading-normal";
  }
  &__trigger {
    @apply "hidden <sm:flex absolute top-4 right-0 sm:hidden";
  }
  &__brand {
    @apply "inline-flex";
  }
}
</style>