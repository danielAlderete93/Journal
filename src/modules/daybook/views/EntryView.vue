<template>
  <div class="entry-title d-flex justify-content-between p-2">
    <div>
      <span class="text-success fs-3 fw-bold">15</span>
      <span class="mx-1 fs-3">Julio</span>
      <span class="mx-2 fs-4 fw-light">2021, Jueves</span>
      <div>
        <button class="btn btn-danger mx-2"> Borrar
          <i class="fa fa-trash-alt"></i>
        </button>

        <button class="btn btn-primary"> Subir foto
          <i class="fa fa-upload"></i>
        </button>
      </div>
      <hr/>
      <div class="d-flex flex-column px-3 h-75">
        <textarea placeholder="¿Qué paso hoy?"></textarea>
      </div>
    </div>
  </div>
  <fab-daybook icon="fa-save"/>
  <img src="https://www.aventuravertical.com/wp-content/uploads/2019/12/monta%C3%B1as-de-mexico-696x400.jpg"
       alt="Entry-picture"
       class="img-thumbnail"
  >
</template>

<script>
import {defineAsyncComponent} from "vue";

export default {
  name: "EntryView",
  components: {
    FabDaybook: defineAsyncComponent(() => import('@/modules/daybook/components/FabDaybook'))
  }
}
</script>

<style lang="scss" scoped>
textarea {
  font-size: 20px;
  border: none;
  height: 100%;

  &:focus {
    outline: none;
  }
}

img {
  width: 200px;
  position: fixed;
  bottom: 150px;
  right: 20px;
  box-shadow: 0 5px 10px rgba($color: #000, $alpha: 0.2);
}
</style>