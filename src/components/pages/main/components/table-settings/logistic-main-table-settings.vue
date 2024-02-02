<script>
import { defineComponent } from 'vue'

import logisticMainTableSettingsPopup from "./logistic-main-table-settings-popup.vue";
import LogisticMainTableSettingsPopup from "./logistic-main-table-settings-popup.vue";

export default defineComponent({
  name: "logistic-main-table-settings",

  components: {
    LogisticMainTableSettingsPopup
  },

  data() {
    return {
      popupIsShown: false
    }
  },

  methods: {
    handleSettingsButtonClick(e) {
      this.popupIsShown = !this.popupIsShown

      e.preventDefault()
      e.stopPropagation()

      if (this.popupIsShown) {
        document.addEventListener('click', this.closePopup)
      }
    },

    closePopup(e) {
      const targetElement = e.target
      const popup = this.$refs.popup.$el

      const isClickWasInPopup = popup.contains(targetElement)

      if (isClickWasInPopup) {
        return
      }

      this.popupIsShown = false

      document.removeEventListener('click', this.closePopup)
    }
  }
})
</script>

<template>
  <div class="logistic-main-table-settings">
    <div class="button" @click="handleSettingsButtonClick"></div>

    <logistic-main-table-settings-popup
        ref="popup"
        v-show="popupIsShown"
        class="popup"
    />
  </div>
</template>

<style scoped lang="sass">
.logistic-main-table-settings
  position: relative

  .button
    width: 15px
    height: 15px
    cursor: pointer
    +background-image-settings()
    background-size: contain
    background-image: url("/assets/images/svg/settings.svg")

  .popup
    position: absolute
    top: 20px
    right: 0
</style>