<template>
    <div class="min-h-screen flex items-center justify-center">
      <div class="bg-gray-600 p-8 rounded-lg shadow-md w-full max-w-sm">
        <h2 class="text-2xl font-bold text-center mb-6">Login</h2>
        <form @submit.prevent="handleLogin" class="space-y-4">
          <!-- Username Field -->
          <div>
            <label for="username" class="block text-sm font-medium">Username</label>
            <input
              type="text"
              id="username"
              v-model="username"
              required
              class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm"
              placeholder="Enter your username"
            />
          </div>
  
          <!-- Password Field -->
          <div>
            <label for="password" class="block text-sm font-medium">Password</label>
            <input
              type="password"
              id="password"
              v-model="password"
              required
              class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm"
              placeholder="Enter your password"
            />
          </div>
  
          <!-- Error Message -->
          <p v-if="errorMessage" class="text-red-500 text-sm">{{ errorMessage }}</p>
  
          <!-- Submit Button -->
          <button
            type="submit"
            class="w-full bg-indigo-600 text-white py-2 px-4 rounded-md hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
          >
            Login
          </button>
        </form>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        username: '',
        password: '',
        errorMessage: ''
      }
    },
    methods: {
      handleLogin() {
        // Simulasi validasi login
        if (this.username === 'admin' && this.password === 'password') {
          this.errorMessage = '';
          this.$emit('login-success'); // Emit event ke halaman induk
        } else {
          this.errorMessage = 'Invalid username or password';
        }
      }
    }
  }
  </script>