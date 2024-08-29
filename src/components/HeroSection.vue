<template>
    <section class="container mx-auto px-0 m-0 flex flex-col md:flex-row h-full w-screen">
      <!-- Left Section -->
      <div class="md:w-1/2 bg-gray-100 flex flex-col justify-center p-10">
        <h1 class="text-4xl md:text-5xl font-bold text-gray-800 mb-4">
          Level Up Your Job Hunt
        </h1>
        <p class="text-sm text-gray-600 mb-6">
          Stop juggling applications, missing deadlines, and struggling to stand out. Our app centralizes everything, keeps you organized with reminders, and provides tools and templates to craft compelling applications that make you a top contender.
        </p>
       <button type="button" class="text-white bg-gray-800 hover:bg-gray-900 focus:outline-none focus:ring-4 focus:ring-gray-300 font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-gray-800 dark:hover:bg-gray-700 dark:focus:ring-gray-700 dark:border-gray-700">
            Take Control of Your Job Search
        </button>
      </div>
      <!-- Right Section -->
      <div class="md:w-1/2 bg-yellow-100 flex items-center justify-center p-8">
        <img 
          :src="heroImage" 
          alt="Hero image description"
          class="w-full h-full object-cover rounded-lg shadow-lg"
        >
      </div>
    </section>
</template>

<script setup>
import heroImage from '@/assets/hero1.jpg'
</script>

