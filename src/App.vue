<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "App"
})
</script>

<template>
  <div class="mainContainer">

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
