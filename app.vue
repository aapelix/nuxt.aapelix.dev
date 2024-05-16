<script setup lang="ts">
useHead({
  titleTemplate: (titleChunk) => {
    return titleChunk ? `${titleChunk} - aapelix.dev` : 'aapelix.dev';
  }
})
</script>

<template>
  <div class="font-mono bg-[#09090b] w-screen h-screen text-[#f3f3f3] overflow-x-hidden animate-fade-up">
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
    opacity: 0;
    filter: blur(1rem);
  }

  :root {
    scroll-behavior: smooth;
    font-family: "Noto Sans Mono", monospace;
    background: #09090b;
  }

  * {
    -ms-overflow-style: none;
  }

  ::-webkit-scrollbar {
    display: none;
  }
</style>
