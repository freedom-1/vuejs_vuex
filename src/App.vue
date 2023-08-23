<template>
  <div class="container mt-4">
    <Navbar />
    <RouterView />
  </div>
</template>

<script>
import { Navbar } from '@/components'
import { RouterView } from 'vue-router'
export default {
  components: { Navbar },
}
</script>

<style></style>
