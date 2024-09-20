<script setup lang="ts">
import { ref } from 'vue';

interface UpdateEntry {
  date: string;
  title: string;
  description: string;
  imageUrl: string;
}

const updates = ref<UpdateEntry[]>([
  {
    date: '25-08-2024',
    title: 'LIVE SET @ ELECTRO HAVEN',
    description: 'A 2-hour electrifying live set at Electro Haven, bringing fresh beats to an epic crowd!',
    imageUrl: 'https://example.com/electrohaven.jpg',
  },
  {
    date: '10-07-2024',
    title: 'SUMMER BEATS MIX VOL. 5',
    description: 'The latest installment of the Summer Beats series is here. Perfect for sunny vibes and good times.',
    imageUrl: 'https://example.com/summerbeats.jpg',
  },
  {
    date: '14-02-2024',
    title: 'BEHIND THE SCENES: TOURING IN EUROPE',
    description: 'A deep dive into the challenges and excitement of my 2024 European tour, from sold-out shows to new collaborations.',
    imageUrl: 'https://example.com/eurotour.jpg',
  },
  {
    date: '02-11-2023',
    title: 'STUDIO SESSIONS: NEW ALBUM TEASER',
    description: 'Get a sneak peek at my upcoming album with exclusive behind-the-scenes studio sessions.',
    imageUrl: 'https://example.com/studiosession.jpg',
  },
]);


</script>

<template>
  <div class="max-w-7xl mx-auto p-4">
    <h2 class="text-3xl font-bold mb-8 text-center">UPDATES</h2>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
      <div v-for="(update, index) in updates" :key="index" class="space-y-2">
        <img :src="update.imageUrl" alt="update image" class="w-full h-56 object-cover" />
        <div class="text-sm text-gray-600">{{ update.date }}</div>
        <h3 class="text-lg font-semibold">{{ update.title }}</h3>
        <p class="text-sm text-gray-600">{{ update.description }}</p>
        <a href="#" class="text-sm text-blue-600 font-semibold hover:underline">READ MORE</a>
      </div>
    </div>
    <button class="mt-8 px-4 py-2 border border-gray-400 hover:border-gray-600 transition-colors text-sm mx-auto block">
      SHOW ALL
    </button>
  </div>
</template>
