<template>
  <a 
    href="#" 
    target="_blank" 
    rel="noopener noreferrer"
    class="group relative flex w-full items-center gap-4 rounded-xl border border-gray-700 bg-sky-300 p-4 shadow-md shadow-sky-500/50 hover:scale-[1.02] hover:shadow-xl transition-all duration-300 hover:border-purple-700 hover:shadow-purple-700/20"
    >
  <!-- Icon Container -->
    <div class="flex h-12 w-12 shrink-0 items-center justify-center rounded-lg bg-blue-500 text-blue-900 transition-all duration-300 group-hover:scale-110 group-hover:bg-sky-400 group-hover:text-blue-500 group-hover:shadow-xl group-hover:shadow-sky-600/50">
      <svg 
        viewBox="0 0 32 32" 
        fill="none" 
        stroke="currentColor" 
        class="h-6 w-6 transition-transform duration-300 group-hover:rotate-6"
      >
        <path d="M30.48 1.53H32v6.09h-1.52Zm-1.52 6.09h1.52v1.53h-1.52Zm-25.91 6.1v9.14h1.53v3.05H6.1v3.05h1.52v1.52h3.05V32h10.67v-1.52h3.05v-1.52h1.52v-3.05h1.52v-3.05h1.53v-9.14h-1.53v3.05h-1.52v1.52h-1.52v-3.05h-1.53v-1.52H9.15v1.52H7.62v3.05H6.1v-1.52H4.58v-3.05Zm6.1 6.09h1.52v-3.04h4.57v-1.53h1.53v1.53h4.57v1.52h1.52v4.57h-1.52v1.52h-3.05v-1.52h-4.57v1.52h-3.05v-1.52H9.15ZM27.43 9.15h1.53v1.52h-1.53Zm-1.52-4.58h1.52V6.1h-1.52Zm-4.57 6.1h6.09v1.52h-6.09Zm3.05-4.57h1.52v1.52h-1.52Zm-1.53 1.52h1.53v1.53h-1.53Zm0-4.57h1.53v1.52h-1.53Zm-1.52 1.52h1.52V6.1h-1.52Zm-1.53 4.58h1.53v1.52h-1.53ZM18.29 0h12.19v1.53H18.29Z"/>
        <path d="M18.29 18.29h1.52v1.52h-1.52Zm0-10.67h1.52v1.53h-1.52Zm0-6.09h-1.52v1.52h-1.53V1.53h-1.52v6.09h1.52V4.57h1.53v3.05h1.52zm-3.05 18.28h3.05v1.53h-3.05Zm-1.52-9.14h4.57v1.52h-4.57ZM12.2 7.62h1.52v1.53H12.2Zm-1.53 1.53h1.53v1.52h-1.53ZM9.15 4.57h1.52V6.1H9.15Zm-4.57 6.1h6.09v1.52H4.58ZM7.62 6.1h1.53v1.52H7.62ZM6.1 7.62h1.52v1.53H6.1Zm0-4.57h1.52v1.52H6.1ZM4.58 4.57H6.1V6.1H4.58ZM3.05 9.15h1.53v1.52H3.05ZM1.53 0h12.19v1.53H1.53Zm0 7.62h1.52v1.53H1.53ZM0 1.53h1.53v6.09H0Z"/>
      </svg>
    </div>

  <!--Text Content -->
    <div class="min-w-0 flex-1">
      <h3 class="font-display truncate font-semibold text-blue-700">Link Title</h3>
      <p class="truncate text-sm text-blue-600">
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia libero hic quo sunt. 
      </p>
    </div>

  <!-- Hover Glow Effect -->
   <div class="absolute inset-0 rounded-xl bg-linear-to-r from-purple-600/0 via-purple-500/10 to-purple-600/20 opacity-0 transition-opacity duration-300 group-hover:opacity-100" />
  </a>
</template>