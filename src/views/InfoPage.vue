<script setup>
  import{ ref } from 'vue'

  const Bio = ref({
    name: "Jorge A Coronado",
    avatar: 'https://api.dicebear.com/9.x/toon-head/svg?seed=anikan&backgroundColor=6a4c93&clothesColor=0b3286&eyes=wink&mouth=smile',
    about: `I have experience developing modern web applications using Vue.js, Node.js, Tailwind CSS, HTML, CSS, and JavaScript. 
            My background allows me to design responsive and user-focused interfaces while also understanding server-side logic and 
            application structure. I use Git for version control and Python for additional programming projects and backend concepts. 
            I also have experience with Blender, which strengthens my understanding of visual design, layout, and spatial thinking in digital environments.`,
    skills: ['Vue.js', 'Node.js', 'Tailwind CSS', 'Git', 'HTML', 'CSS', 'JavaScript', 'Python', 'blender'],
    email: 'JCoronado_2294@stu.southtexascollege.edu',
    location: 'Mission, Tx'
  })
</script>

<template>
  <main class="flex min-h-screen flex-col items-center px-4 py-8 sm:py-12">
    <RouterLink
      to="/"
      class="my-8 self-start text-sm text-gray-300 underline-offset-4 hover:text-[#4cc9f0] hover:underline transition-colors duration-200"
      >👈 Back to links
    </RouterLink>

    <!-- Profile Card -->
    <div class="w-full max-w-lg rounded-2xl border border-purple-400 bg-blue-500 p-6 shadow-xl shadow-purple-800/50 sm:p-8">

    <!-- Header -->
      <div class="mb-6 flex-col items-center text-center sm:flex-row sm:text-left">
        <div class="h-20 w-20 shrink-0 overflow-hidden rounded-full border-4 border-blue-400 shadow-lg shadow-blue-500/20 sm:mr-6 sm:mb-0">
          <img
            :src="Bio.avatar"
            :alt="Bio.name"
            class="h-full w-full object-cover"
          />
        </div>
        <div>
          <h1 class="mb-1 font-display text-2xl font-bold text-white">{{ Bio.name }}</h1>
          <p class="text-sm text-gray-300">📌 {{ Bio.location }}</p>
        </div>
      </div>

    <!-- About Section -->
      <div class="mb-6">
        <h2 class="mb-3 text-lg font-semibold text-white">About</h2>
        <p class="leading-relaxed text-gray-300">{{ Bio.about }}</p>
      </div>

    <!-- Skills Section -->
      <div class="mb-6">
        <h2 class="mb-3 text-lg font-semibold text-white">Skills</h2>
        <div class="flex flex-wrap gap-2">
          <span
            v-for="skill in Bio.skills"
            :key="skill"
            class="rounded-full bg-blue-600 px-3 py-1 text-sm text-white"
          >
            {{ skill }}
          </span>

        </div>
      </div>

    <!-- Contact -->
      <div>
        <h2 class="mb-3 text-lg font-semibold text-white">Get in Touch</h2>
        <a
          :href="`mailto:${Bio.email}`"
          class="group inline-flex items-center gap-2 rounded-xl bg-blue-600 px-6 py-3 font-medium text-white shadow-lg shadow-purple-600/40 transition-all duration-200 hover:bg-blue-700/30 hover:scale-105 hover:shadow-xl hover:shadow-purple-700/60 active:scale-95"
        >
          <svg 
            xmlns="http://www.w3.org/2000/svg" 
            fill="none" 
            viewBox="0 0 24 24" 
            stroke-width="1.5" 
            stroke="currentColor" 
            class="h-5 w-5 transition-transform duration-200 group-hover:rotate-12"
            >
              <path stroke-linecap="round" 
              stroke-linejoin="round" 
              d="M21.75 6.75v10.5a2.25 2.25 0 0 1-2.25 2.25h-15a2.25 2.25 0 0 1-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0 0 19.5 4.5h-15a2.25 2.25 0 0 0-2.25 2.25m19.5 0v.243a2.25 2.25 0 0 1-1.07 1.916l-7.5 4.615a2.25 2.25 0 0 1-2.36 0L3.32 8.91a2.25 2.25 0 0 1-1.07-1.916V6.75" 
              />
          </svg>
          Send Email
      </a>
      </div>
    </div>
  </main>
</template>
