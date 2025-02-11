<template>
    <div>
      <LoginForm @login-success="redirectToDashboard" />
    </div>
  </template>
  
  <script>
  import LoginForm from '~/components/LoginForm.vue'
  
  export default {
    components: {
      LoginForm
    },
    methods: {
      redirectToDashboard() {
        this.$router.push('/'); // Redirect ke halaman utama setelah login berhasil
      }
    }
  }
  </script>