<template>
    <div class="min-h-screen flex flex-col bg-black text-white">
      <!-- Header -->
      <Header />
  
      <!-- Main Content -->
      <main class="flex-grow">
        <slot />
      </main>
  
      <!-- Footer -->
      <Footer />
    </div>
  </template>
  
  <script>
  import Header from '~/components/Header.vue'
  import Footer from '~/components/Footer.vue'
  
  export default {
    components: {
      Header,
      Footer
    }
  }
  </script>
  
  <style>
  body {
    margin: 0;
    font-family: Arial, sans-serif;
  }
  </style>