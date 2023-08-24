<template>
  <main class="form-signin w-25 m-auto text-center text-primary">
    <form>
      <img class="mb-4" :src="logo" alt="" width="150" height="60" />
      <h1 class="h3 mb-3 fw-normal">Register</h1>

      <Input :label="'Ismingiz'" :type="'text'" />
      <Input :label="'Email address'" :type="'email'" />
      <Input :label="'Parol'" :type="'password'" />

      <Button type="submit" :disabled="isLoading" @click="submitHandler"
        >Ro`yxatdan o`tish</Button
      >
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
  computed: {
    isLoading() {
      return this.$store.state.auth.isLoading
    },
  },
  methods: {
    submitHandler(e) {
      e.preventDefault()
      this.$store.dispatch('register')
    },
  },
}
</script>

<style></style>
