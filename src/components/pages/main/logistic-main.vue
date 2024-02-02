<script>
import { defineComponent } from 'vue'

import logisticLeftMenu from "../../ui-kit/logistic-left-menu.vue";

import logisticMainHeader from "./components/header/logistic-main-header.vue";

import logisticMainNavigation from "./components/navigation/logistic-main-navigation.vue";
import logisticMainTableSettings from "./components/table-settings/logistic-main-table-settings.vue";

import logisticMainButtonsGroup from "./components/buttons/logistic-main-buttons-group.vue";

export default defineComponent({
  name: "logistic-main",

  components: {
    logisticLeftMenu,

    logisticMainHeader,

    logisticMainNavigation,
    logisticMainTableSettings,

    logisticMainButtonsGroup
  }
})
</script>

<template>
  <div class="logistic-main">
    <logistic-left-menu />

    <main>
      <logistic-main-header />

      <div class="nav-bar">
        <logistic-main-navigation />

        <logistic-main-table-settings class="settings" />
      </div>

      <logistic-main-buttons-group />
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
    display: flex
    flex-direction: column
    gap: 25px
    background-color: $backgroundWhite

    @media (min-width: $largeResolutionStart)
      padding: 25px

    @media (max-width: $mediumResolutionEnd)
      padding: 16px 10px

    .nav-bar
      width: 100%

      @media (min-width: $largeResolutionStart)
        display: flex
        justify-content: space-between
        gap: 30px

      .settings
        @media (max-width: $mediumResolutionEnd)
          display: none
</style>