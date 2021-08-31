
<script setup lang="ts">
import { Popover, PopoverButton, PopoverPanel } from '@headlessui/vue'
import { useRouter } from 'vue-router'
import { useI18n } from 'vue-i18n'
const { t } = useI18n()
const router = useRouter()

</script>

<template>
  <Popover class="relative z-20">
    <PopoverButton>
      <ic:round-menu class="h-6 w-6" />
    </PopoverButton>

    <transition
      enter-active-class="transition duration-200 ease-out"
      enter-from-class="translate-y-1 opacity-0"
      enter-to-class="translate-y-0 opacity-100"
      leave-active-class="transition duration-150 ease-in"
      leave-from-class="translate-y-0 opacity-100"
      leave-to-class="translate-y-1 opacity-0"
    >
      <PopoverPanel
        class="absolute z-30 w-52 -right-2 sm:px-0 "
      >
        <div
          class="bg-white z-50 overflow-hidden text-left rounded-lg shadow-lg border-2 border-blue-300/50 "
        >
          <div class="w-full text-lg font-medium py-3 px-3 ">
            {{ t('hello') }}, {{ name }}
          </div>
          <div
            class="w-full text-base pt-2 pb-3 px-5 border-t border-blue-300/50"
            @click="router.push('/doclist')"
          >
            {{ t('button.list') }}
          </div>
          <div
            v-if="!router.currentRoute.value.path.includes('/add-paper')"
            class="w-full text-base pt-2 pb-3 px-5 border-t border-blue-300/50"
            @click="router.push('/add-paper')"
          >
            {{ t('button.new') }}
          </div>
          <div
            class="w-full text-base cursor-pointer py-2 px-5 border-t border-blue-300/50"
            @click="router.push('/auth/Manageprofile')"
          >
            {{ t('button.profile') }}
          </div>
        </div>
      </PopoverPanel>
    </transition>
  </Popover>
</template>
