<template>
  <div class="d-flex justify-content-center">
    <h1 class="align-self-center "> No hay nada seleccionado</h1>
    <button-new-entry-daybook/>
  </div>
</template>

<script>
import {defineAsyncComponent} from "vue";

export default {
  name: "NoEntrySelected",
  components: {
    ButtonNewEntryDaybook: defineAsyncComponent(() => import('@/modules/daybook/components/FabDaybook'))
  }
}
</script>

<style scoped>
div {
  height: 100%;
}

</style>