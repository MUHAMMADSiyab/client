<template>
  <h1>Welcome {{ $auth.user.name }}</h1>
</template>

<script>
export default {
  mounted() {
    this.$axios
      .get('api/test', { withCredentials: true })
      .then((data) => console.log(data))
      .catch((err) => console.log(err))
  },
}
</script>