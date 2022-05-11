<script setup>
import {ref} from "vue"
import {Switch} from "@headlessui/vue";

const enabled = ref(false)
</script>

<template>
  <Switch>
    <div class="block">
      <Switch
          v-model="enabled"
          :class="enabled ? 'text-blue-500' : 'text-gray-900'"
          class="h-16 leading-normal px-4 py-2 rounded-md text-sm font-medium focus:outline-none"
      >
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"
             stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round"
                d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"/>
        </svg>
      </Switch>
    </div>
  </Switch>
</template>

<style scoped>

</style>
