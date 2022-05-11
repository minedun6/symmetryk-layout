<template>
  <Popover v-slot="{open}" class="relative">
    <div class="block">
      <PopoverButton
          type="button"
          class="h-16 leading-normal px-4 py-2 rounded-md text-sm font-medium text-gray-900 focus:outline-none"
      >
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"
             stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round" d="M5 5a2 2 0 012-2h10a2 2 0 012 2v16l-7-3.5L5 21V5z"/>
        </svg>
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
            class="absolute left-1/2 z-10 mt-3 w-screen max-w-3xl -translate-x-1/2 transform p-4 border rounded">
          Bookmarks
        </PopoverPanel>
      </transition>
    </div>
  </Popover>
</template>

<script setup>
import {PopoverButton, Popover, PopoverPanel} from '@headlessui/vue'
</script>

<style scoped>

</style>
