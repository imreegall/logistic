<script>
import { defineComponent } from 'vue'

import logisticMainButtonsGroupButton from "./logistic-main-buttons-group-button.vue";

export default defineComponent({
  name: "logistic-main-buttons-group",

  components: {
    logisticMainButtonsGroupButton
  }
})
</script>

<template>
  <div class="logistic-main-buttons-group">
    <logistic-main-buttons-group-button />
  </div>
</template>

<style scoped lang="sass">
.logistic-main-buttons-group
  width: 100%
  display: flex
  gap: 20px
  padding: 20px 25px
  background-color: white
  border: solid 1px var(--pale-grey)
  box-shadow: 0 5px 20px 0 rgba(0, 0, 0, 0.07)
  +border-radius(10px)
</style>