<template>
  <div id="app" class="flex flex-col min-h-screen">

    <router-view />
    
    <footer class="bg-gray-800 text-white py-4 text-center">
      <p>&copy; 2024 Your Company. All rights reserved.</p>
    </footer>
  </div>
</template>

<script setup>
</script>

<style scoped>
.min-h-screen {
  min-height: 100vh;
}
footer {
  margin-top: auto; /* Push footer to the bottom */
}
body {
  margin: 0;
}
</style>
