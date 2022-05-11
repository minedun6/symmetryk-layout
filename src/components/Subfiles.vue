<template>
  <Popover v-slot="{open}" class="relative">
    <div class="block">
      <PopoverButton
          type="button"
          class="h-16 leading-normal px-4 py-2 rounded-md text-sm font-medium text-gray-900 focus:outline-none"
      >
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"
             stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round"
                d="M8 7v8a2 2 0 002 2h6M8 7V5a2 2 0 012-2h4.586a1 1 0 01.707.293l4.414 4.414a1 1 0 01.293.707V15a2 2 0 01-2 2h-2M8 7H6a2 2 0 00-2 2v10a2 2 0 002 2h8a2 2 0 002-2v-2"/>
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
            class="absolute z-10 mt-3 w-screen max-w-sm px-4 sm:px-0 lg:max-w-3xl left-auto right-0">
          <div class="overflow-hidden rounded-lg shadow-lg ring-1 ring-black ring-opacity-5">
            <div class="relative grid gap-8 bg-white p-7">
              
            </div>
          </div>
        </PopoverPanel>
      </transition>
    </div>
  </Popover>
</template>

<script setup>
import {dayjs as moment} from 'dayjs'
import {v4 as uuid} from 'uuid'
import {PopoverButton, Popover, PopoverPanel} from '@headlessui/vue'

const subFiles = [
  {
    id: uuid(),
    name: 'SubFile #1',
    index: 0,
    createdAt: moment().format('YYYY-MM-DD hh:mm:ss'),
    state: 1,
    pages: [
      {
        file_is_off_label: false,
        file_id: null,
        filename: 'Cover',
        page_number: 1,
        page: 1,
        page_is_off_label: false
      },
      {
        file_is_off_label: false,
        file_id: 3009,
        filename: 'MI-Touch-CLM-Content-Guidelines-v.1.6.2.pdf',
        page_number: 2,
        page: 2,
        page_is_off_label: false
      },
      {
        file_is_off_label: true,
        file_id: 6567,
        filename: "1700.full.pdf",
        page_number: 3,
        page: 5,
        page_is_off_label: true
      },
      {
        file_is_off_label: true,
        file_id: 6567,
        filename: "1700.full.pdf",
        page_number: 4,
        page: 3,
        page_is_off_label: false
      },
      {
        file_is_off_label: true,
        file_id: 6567,
        filename: "1700.full.pdf",
        page_number: 5,
        page: 6,
        page_is_off_label: false
      },
      {
        file_is_off_label: true,
        file_id: 6567,
        filename: "1700.full.pdf",
        page_number: 6,
        page: 9,
        page_is_off_label: false
      }
    ]
  }
]
</script>

<style scoped>

</style>
