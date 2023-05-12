<template>
  <q-layout view="lHh Lpr lFf">
    
     <!-- <q-page-sticky  position="bottom-right" class=" tw-z-10" :offset="fabPos">
        <q-btn fab-mini icon="directions" class="bg-primary" color="primary" style="box-shadow:1px 1px 4px #0086cf77;"
          :disable="draggingFab" v-touch-pan.prevent.mouse="moveFab"
          unelevated dense  @click="$router.push('/')" />
      </q-page-sticky> -->
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MainLayout',


  setup () {
    const fabPos = ref([ 20, 20 ])
    const draggingFab = ref(false)
    return {
           fabPos,
      draggingFab,
      moveFab (ev) {
        draggingFab.value = ev.isFirst !== true && ev.isFinal !== true

        fabPos.value = [
          fabPos.value[ 0 ] - ev.delta.x,
          fabPos.value[ 1 ] - ev.delta.y
        ]
      }
    }
  }
})
</script>
<style>
@import "tailwindcss/base";
@import "tailwindcss/components";
@import "tailwindcss/utilities";
</style>
