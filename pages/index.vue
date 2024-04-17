<script lang="ts">
import {refreshNuxtData, useAsyncData} from "#app";

export default defineNuxtComponent({
  async setup() {
    onMounted(() => {
      refreshNuxtData()
    })

    await useAsyncData(async () => {
      console.log('first')
      return true
    })
  }
})
</script>

<template>
<nuxt-link to="/second">
  Go to second page
</nuxt-link>
</template>
