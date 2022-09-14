<template>
  <div class="entry-list-container">
    <div class="px-2 pt-2">
      <input type="text" class="form-control" placeholder="Buscar entrada">
    </div>
    <div class="entry-scrollarea">
      <button-float-daybook
          v-for="item in 100"
          :key="item"
      >

        Entry
      </button-float-daybook>

    </div>
  </div>
</template>

<script>
import {defineAsyncComponent} from "vue";

export default {
  name: "EntryList",
  components: {
    ButtonFloatDaybook: defineAsyncComponent(() => import('@/modules/daybook/components/EntryDaybook'))
  }
}
</script>

<style lang="scss" scoped>

.entry-list-container {
  border-right: 1px solid #2c3e50;
  height: calc(100vh - 56px);
}

.entry-scrollarea {
  height: calc(100vh - 120px);
  overflow: scroll;
}


</style>