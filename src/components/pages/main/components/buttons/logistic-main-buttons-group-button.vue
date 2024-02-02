<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: "logistic-main-buttons-group-button"
})
</script>

<template>
  <div class="logistic-main-buttons-group-button">
    <div class="plus-icon"></div>

    <h2 class="title">Добавить строку</h2>
  </div>
</template>

<style scoped lang="sass">
.logistic-main-buttons-group-button
  background-color: $mainButtonBackground
  +border-radius(5px)
  padding: 10px 15px 10px 10px
  gap: 7px
  display: flex
  align-items: center
  cursor: pointer
  +user-select(none)

  .plus-icon
    width: 11px
    height: 11px
    +background-image-settings()
    background-image: url("/assets/images/svg/plus.svg")

  > .title
    font-size: 14px
    color: white
</style>