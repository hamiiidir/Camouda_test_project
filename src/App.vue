<template>
  <div dir="rtl" style="font-family: yekan">
    <Home />
  </div>
</template>

<script lang="ts">
  import { defineComponent } from '@vue/runtime-core'
  import Home from './components/Home/Home.vue'

  export default defineComponent({
    components: {
      Home
    },
  })

</script>

