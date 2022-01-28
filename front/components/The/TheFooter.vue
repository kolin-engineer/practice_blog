<template lang="pug">
footer.footer
  .footer__inner
    .socials
      a.social
        b-icon(icon="facebook", href="", size="is-medium") 
      a.ml-4.social
        b-icon(icon="twitter", href="", size="is-medium")
      a.ml-4.social
        b-icon(icon="linkedin", href="", size="is-medium")
    p.copy.mt-4 Copyright ©2022 All rights reserved
</template>

<script>
import { defineComponent } from "@vue/composition-api";

export default defineComponent({
  setup() {},
});
</script>

<style lang="scss" scoped>
.footer {
  @apply "text-xs py-12 flex flex-col items-center";
}
.socials {
  @apply "flex justify-between";
}
.social {
  @apply "text-black hover:text-indigo-600";
}
</style>
