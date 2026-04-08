<script setup>
import { ref } from 'vue' // You’re importing the ref function from Vue so you can create reactive variables.
import LinkCard from '@/components/LinkCard.vue'

const profile = ref({
  name: 'Jorge A Coronado',
  slogan: 'Web Developer and Programmer',
  avatar:
    'https://api.dicebear.com/9.x/toon-head/svg?seed=anikan&backgroundColor=6a4c93&clothesColor=0b3286&eyes=wink&mouth=smile',
  links: [
    {
      id: 1,
      title: 'GitHub',
      url: 'https://github.com/JorgeACoronado/',
      icon: 'code',
      description: 'Checkout my projects',
    },
    {
      id: 2,
      title: 'LinkedIn',
      url: 'https://www.linkedin.com/in/jorge-coronado-5aab26343/',
      icon: 'briefcase',
      description: 'Connect with me professionally',
    },
    {
      id: 3,
      title: 'Even Tab Split in Vue',
      url: 'https://even-tab-split.jcoronado2294.workers.dev/',
      icon: 'project',
      description: 'See my Project',
    },
  ],
})
</script>

<template>
  <main class="flex min-h-screen flex-col items-center px-4 py-8">
    <!-- Profile Header -->
    <div class="mb-8 flex flex-col items-center text-center">
      <div
        class="mb-4 h-24 w-24 overflow-hidden rounded-full border-4 border-blue-400 shadow-lg shadow-blue-500/20 sm:h-32 sm:w-32"
      >
        <img
          :src="profile.avatar"
          :alt="profile.name"
          class="h-full w-full object-cover"
        />
      </div>
      <h1 class="mb-2 font-display text-2xl font-bold text-[#4cc9f0]">{{ profile.name }}</h1>
      <p class="max-w-xs text-gray-300 sm:text-lg">{{ profile.slogan }}</p>
    </div>

    <!-- Links List -->
    <div class="flex w-full max-w-md flex-col gap-4">
      <LinkCard
        v-for="link in profile.links"
        :key="link.id"
        :title="link.title"
        :url="link.url"
        :description="link.description"
        :icon="link.icon"
      />
    </div>

    <!--Navigate to Info-->
    <RouterLink
      to="/info"
      class="mt-8 text-sm text-gray-300 underline-offset-4 transition-colors duration-200 hover:text-[#4cc9f0] hover:underline"
      >About me 🖖
    </RouterLink>
  </main>
</template>
