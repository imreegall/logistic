<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: "logistic-left-menu"
})
</script>

<template>
  <div class="logistic-left-menu">

  </div>
</template>

<style scoped lang="sass">
.logistic-left-menu
  @media (min-width: $largeResolutionStart)
    width: 229px
    background: radial-gradient(circle at 29% 0, #000, #1c2734 103%)
    position: sticky
    top: 0
    height: 100vh

  @media (max-width: $mediumResolutionEnd)
    display: none
</style>