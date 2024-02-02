<script>
import { defineComponent } from "vue";

import logisticMain from "./components/pages/main/logistic-main.vue";

export default defineComponent({
  name: "App",

  components: {
    logisticMain
  }
})
</script>

<template>
  <div class="mainContainer">
    <logistic-main />
  </div>
</template>

<style lang="sass">
#app
  display: flex
  justify-content: center
  width: 100%

  .mainContainer
    display: flex
    flex-direction: column
    align-items: center
    width: 100%
    min-height: 100vh
</style>
