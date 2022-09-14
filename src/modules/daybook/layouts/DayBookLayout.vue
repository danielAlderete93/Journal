<template>
  <navbar-daybook/>
  <div class="d-flex">
    <div class="col-4">
      <entry-list/>
    </div>
    <div class="col">
      <router-view/>
    </div>
  </div>
</template>

<script>
import {defineAsyncComponent} from 'vue'


export default {

  name: "DayBookLayout",
  components: {
    navbarDaybook: defineAsyncComponent(() => import("@/modules/daybook/components/NavbarDaybook")),
    entryList: defineAsyncComponent(() => import("@/modules/daybook/components/EntryListDaybook"))
  }
}


</script>

<style scoped>

</style>