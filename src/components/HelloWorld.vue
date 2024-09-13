<script setup lang="ts">
function handleClick() {
  alert("Button clicked!");
}
</script>

<template>
  <div class="p-6 max-w-sm mx-auto bg-white rounded-xl shadow-md space-y-4">
    <div class="text-center">
      <h1 class="text-xl font-bold text-gray-900">Hello, Tailwind CSS!</h1>
      <p class="text-gray-600">
        This is an example of how you can use Tailwind CSS in a Vue component.
      </p>
    </div>
    <button
      @click="handleClick"
      class="px-4 py-2 bg-blue-500 text-white rounded hover:bg-blue-700"
    >
      Click Me
    </button>
  </div>
</template>
