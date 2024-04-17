<script lang="ts">
import {useAsyncData} from "#app";

export default defineNuxtComponent({
  async setup() {
    await useAsyncData(async () => {
      console.log('second')
      return true
    })
  }
})
</script>

<template>
  <nuxt-link to="/">
    Go to first page
  </nuxt-link>
</template>
