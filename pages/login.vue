<template>
  <button @click.prevent="login">Login</button>
</template>

<script>
export default {
  methods: {
    login() {
      this.$auth.loginWith('laravelSanctum', {
        data: {
          email: 'john@gmail.com',
          password: 'johnadmin',
        },
      })
    },
  },
}
</script>