<template>
  <div class="d-flex flex-column flex-md-row align-items-center py-3 mb-4 border-bottom">
      <a class="d-flex align-items-center link-body-emphasis text-decoration-none">
        <img :src="logo" alt="logo" class="navcha" @click="onHomeHandler" />
      </a>

      <nav class="d-inline-flex mt-2 mt-md-0 ms-md-auto">
        <RouterLink class="me-3 py-2 link-body-emphasis text-decoration-none" :to="{name:'login'}">Login</RouterLink>
        <RouterLink class="me-3 py-2 link-body-emphasis text-decoration-none" :to="{name:'register'}">Register</RouterLink>
      </nav>
    </div>
</template>

<script>
import { logo } from '@/constants';
export default {
data() {
  return {
    logo,
  }
},
methods: {
  onHomeHandler(){
    return this.$router.push('/')
  }
},
}
</script>

<style scoped>
.navcha{
  width: 100px;
  cursor: pointer;
}
</style>