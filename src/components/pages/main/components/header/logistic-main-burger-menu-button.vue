<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: "logistic-main-burger-menu-button"
})
</script>

<template>
  <div class="logistic-main-burger-menu-button">

  </div>
</template>

<style scoped lang="sass">
.logistic-main-burger-menu-button
  width: 15px
  height: 12px
  +background-image-settings()
  background-size: contain
  background-image: url("/assets/images/svg/burger.svg")
</style>