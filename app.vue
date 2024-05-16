<script setup lang="ts">
useHead({
  titleTemplate: (titleChunk) => {
    return titleChunk ? `${titleChunk} - Site Title` : 'Site Title';
  }
})
</script>

<template>
  <div class="font-mono bg-[#0f0f0f] w-screen h-screen text-[#f3f3f3] overflow-x-hidden">
    <NuxtPage />
  </div>
</template>

<style>
  .page-enter-active,
  .page-leave-active {
    transition: all 0.4s;
  }

  .page-enter-from,
  .page-leave-to {
    transform: translateY(-20px);
    filter: blur(1rem);
  }

  :root {
    scroll-behavior: smooth;
    font-family: "Noto Sans Mono", monospace;
    background: #0f0f0f;
  }

  * {
    -ms-overflow-style: none;
  }

  ::-webkit-scrollbar {
    display: none;
  }
</style>
