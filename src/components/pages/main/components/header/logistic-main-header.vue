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

  @media (min-width: $largeResolutionStart)
    padding: 25px

  @media (max-width: $mediumResolutionEnd)
    display: flex
    gap: 25px
    align-items: baseline
    padding: 16px 30px 25px 10px

  .burger
    @media (min-width: $largeResolutionStart)
      display: none

  > .title
    flex: 1
</style>