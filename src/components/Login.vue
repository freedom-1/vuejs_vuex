<template>
  <main class="form-signin w-25 m-auto text-center text-primary">
    <form>
      <img class="mb-4" :src="logo" alt="logo" width="150" height="60" />
      <h1 class="h3 mb-3 fw-normal">Login</h1>

      <Input :label="'Email address'" :type="'email'" />
      <Input :label="'Parol'" :type="'password'" />

      <Button type="submit">Kirish</Button>
    </form>
  </main>
</template>

<script>
import { logo } from '@/constants'
export default {
  data() {
    return {
      logo,
    }
  },
}
</script>

<style></style>
