<script>
import { defineComponent } from 'vue'

import logisticMainBurgerMenuButton from "./logistic-main-burger-menu-button.vue";

export default defineComponent({
  name: "logistic-main-header",

  components: {
    logisticMainBurgerMenuButton
  }
})
</script>

<template>
  <div class="logistic-main-header">
    <logistic-main-burger-menu-button class="burger" />

    <h2 class="title">Проведение ТО и мелкий ремонт</h2>
  </div>
</template>

<style scoped lang="sass">
.logistic-main-header
  width: 100%
  font-size: 30px
  color: black

  @media (max-width: $mediumResolutionEnd)
    display: flex
    gap: 25px

  .burger
    @media (min-width: $largeResolutionStart)
      display: none

    @media (max-width: $mediumResolutionEnd)
      margin-top: 9px

  > .title
    flex: 1
</style>