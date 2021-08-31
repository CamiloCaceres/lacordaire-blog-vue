<script lang="ts" setup>
const { t } = useI18n()
</script>

<template>
  <div class="py-7 px-10 flex justify-between items-center">
    <div class="flex items-center space-x-2 hover:text-yellow-500 transition-all">
      <p class=" pl-5 font-medium text-xl">
        {{ t('title') }}
      </p>
      <ri:quill-pen-line class="h-6 w-6" />
    </div>

    <HamburguerMenu class="md:hidden" />
    <div class="hidden md:flex space-x-12 px-5 ">
      <div class="border-b-2 border-transparent hover:border-yellow-500 transition-all cursor-pointer">
        posts
      </div>
      <div class="border-b-2 border-transparent hover:border-yellow-500 transition-all cursor-pointer">
        about us
      </div>
      <div class="border-b-2 border-transparent hover:border-yellow-500 transition-all cursor-pointer">
        our school
      </div>
    </div>
  </div>
</template>
