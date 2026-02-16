<script setup>
import { ref } from 'vue'
import LinkCard from '@/components/LinkCard.vue';

const profile = ref({
  name: 'Jorge A Coronado',
  slogan: 'Web Developer and Programmer',
  avatar: 'https://api.dicebear.com/9.x/toon-head/svg?seed=anikan&backgroundColor=6a4c93&clothesColor=0b3286&eyes=wink&mouth=smile',
});
</script>

<template>
  <main class="flex min-h-screen flex-col items-center px-4 py-8">
    <!-- Profile Header -->
    <div class="mb-8 flex flex-col items-center text-center">
      <div class="mb-4 h-24 w-24 overflow-hidden rounded-full border-4 border-blue-400 shadow-lg shadow-blue-500/20 sm:h-32 sm:w-32">
        <img
        :src="profile.avatar"
        :alt="profile.name"
        class="h-full w-full object-cover"
      />
      </div>
      <h1 class="mb-2 font-display text-2xl font-bold text-[#4cc9f0]">{{ profile.name }}</h1>
      <p class="max-w-xs text-gray-300 sm:text-lg">{{ profile.slogan }}</p>
    </div>
  </main>
</template>
