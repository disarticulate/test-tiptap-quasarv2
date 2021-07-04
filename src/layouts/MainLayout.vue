<template>
  <q-layout view="lHh Lpr lFf">
    <IndexPage/>
  </q-layout>
</template>

<script>
import IndexPage from '../pages/Index'
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  components: {
    IndexPage
  },

  setup () {
    const leftDrawerOpen = ref(false)

    return {
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
