<script setup lang="ts">
import { ref } from 'vue';

const isOpen = ref(false);
</script>
<template>
  <div class="min-h-screen flex flex-col md:flex-row bg-gradient-to-br from-blue-100 to-blue-300">
    <!-- Mobile Navbar -->
    <div class="md:hidden flex items-center justify-between p-4">
      <h1 class="text-3xl font-bold">TAILWIND COLLECTIVE</h1>
      <button @click="isOpen = !isOpen" class="text-3xl focus:outline-none">
        &#9776;
      </button>
    </div>

    <!-- Drawer for mobile navigation -->
    <transition name="slide">
      <div
        v-if="isOpen"
        class="fixed inset-0 bg-blue-200 p-6 z-50 flex flex-col space-y-4 text-xl"
      >
        <button @click="isOpen = false" class="self-end text-3xl">&#10005;</button> <!-- Close button -->
        <ul class="space-y-4 text-xl">
          <li class="hover:underline cursor-pointer">AGENDA</li>
          <li class="hover:underline cursor-pointer">WEBSHOP</li>
          <li class="hover:underline cursor-pointer">UPDATES</li>
          <li class="hover:underline cursor-pointer">MUSIC</li>
          <li class="hover:underline cursor-pointer">PHOTOS BY TAILWIND</li>
          <li class="hover:underline cursor-pointer">CONTACT</li>
        </ul>
      </div>
    </transition>

    <!-- Image Section -->
    <div class="md:w-2/3 w-full flex items-center justify-center">
      <img
        src="path-to-your-image.jpg"
        alt="Artists"
        class="max-w-full h-auto object-cover md:h-auto md:max-h-screen"
      />
    </div>

    <!-- Desktop Navbar -->
    <div class="hidden md:flex md:w-1/3 flex-col justify-center items-start p-8">
      <h1 class="text-4xl font-bold mb-8">TAILWIND COLLECTIVE</h1>
      <ul class="space-y-4 text-xl">
        <li class="group relative cursor-pointer">
          <span class="group-hover:text-blue-600">AGENDA</span>
          <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-blue-600 group-hover:w-full transition-all duration-500"></span>
        </li>
        <li class="group relative cursor-pointer">
          <span class="group-hover:text-blue-600">WEBSHOP</span>
          <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-blue-600 group-hover:w-full transition-all duration-500"></span>
        </li>
        <li class="group relative cursor-pointer">
          <span class="group-hover:text-blue-600">UPDATES</span>
          <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-blue-600 group-hover:w-full transition-all duration-500"></span>
        </li>
        <li class="group relative cursor-pointer">
          <span class="group-hover:text-blue-600">MUSIC</span>
          <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-blue-600 group-hover:w-full transition-all duration-500"></span>
        </li>
        <li class="group relative cursor-pointer">
          <span class="group-hover:text-blue-600">PHOTOS BY TAILWIND</span>
          <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-blue-600 group-hover:w-full transition-all duration-500"></span>
        </li>
        <li class="group relative cursor-pointer">
          <span class="group-hover:text-blue-600">CONTACT</span>
          <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-blue-600 group-hover:w-full transition-all duration-500"></span>
        </li>
      </ul>
    </div>
  </div>
</template>
<style scoped>
.slide-enter-active, .slide-leave-active {
  transition: transform 0.3s ease;
}
.slide-enter, .slide-leave-to {
  transform: translateX(100%);
}
</style>
