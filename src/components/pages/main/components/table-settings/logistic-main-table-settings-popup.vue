<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: "logistic-main-table-settings-popup"
})
</script>

<template>
  <div class="logistic-main-table-settings-popup">
    <div class="main-list-el">
      <h2 class="title">Отображение столбцов</h2>

      <div class="chevron"></div>
    </div>

    <div class="main-list-el">
      <h2 class="title">Порядок столбцов</h2>

      <div class="chevron"></div>
    </div>
  </div>
</template>

<style scoped lang="sass">
.logistic-main-table-settings-popup
  +border-radius(5px)
  box-shadow: 0 0 3px 0 #000, inset 0 1px 2px 0 rgba(255, 255, 255, 0.5)
  display: flex
  flex-direction: column
  overflow: hidden
  +user-select(none)

  .main-list-el
    white-space: nowrap
    padding: 7px 10px
    display: flex
    align-items: center
    gap: 9px
    justify-content: space-between
    cursor: pointer

    &:hover
      background-color: $tableSettingsPopupHover

    > .title
      font-size: 14px

    .chevron
      width: 6px
      height: 9px
      cursor: pointer
      +background-image-settings()
      background-size: contain
      background-image: url("/assets/images/svg/arrow-right.svg")
</style>