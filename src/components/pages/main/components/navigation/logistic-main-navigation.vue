<script>
import {defineComponent} from 'vue'

export default defineComponent({
  name: "logistic-main-navigation"
})
</script>

<template>
  <nav class="logistic-main-navigation">
    <h1 class="nav-el">Общее</h1>

    <h1 class="nav-el active">Товар списания</h1>

    <h1 class="nav-el">Доп. расходы</h1>
  </nav>
</template>

<style scoped lang="sass">
.logistic-main-navigation
  width: 100%
  display: flex
  flex-wrap: wrap
  gap: 20px

  .nav-el
    font-size: 16px
    color: $navigationBlue
    cursor: pointer
    +user-select(none)

    &.active
      color: black
</style>