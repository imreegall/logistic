<script>
import { defineComponent } from 'vue'

import logisticLeftMenu from "../../ui-kit/logistic-left-menu.vue";
import logisticMainHeader from "./components/header/logistic-main-header.vue";

export default defineComponent({
  name: "logistic-main",

  components: {
    logisticLeftMenu,
    logisticMainHeader
  }
})
</script>

<template>
  <div class="logistic-main">
    <logistic-left-menu />

    <main>
      <logistic-main-header />
    </main>
  </div>
</template>

<style scoped lang="sass">
.logistic-main
  display: flex
  width: 100%

  main
    flex: 1
    width: 100%
    min-height: 100vh
</style>