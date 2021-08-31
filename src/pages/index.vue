<script setup lang="ts">

// const { t } = useI18n()
</script>

<template>
  <div class="text-left max-w-5xl mx-auto z-10">
    <h1 class="text-5xl font-semibold py-10">
      Lacordaire bilingual school blog
    </h1>
    <div class="border-black border-t-2 w-10 py-5"></div>
    <p class="w-1/2 text-lg">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam justo dui, tincidunt quis arcu vel, suscipit auctor metus. Nunc eleifend elit vitae mauris volutpat, ut efficitur neque pretium
    </p>
    <button class="rounded-full my-12 py-1.5 px-8 bg-gray-900 hover:bg-yellow-500 text-white font-semibold transition-all">
      read us!
    </button>
  </div>
  <img src="../assets/circle.svg" alt="" class="absolute -right-32 bottom-1 h-3/4 opacity-50 z-0">
</template>

<route lang="yaml">
meta:
  layout: home
</route>
