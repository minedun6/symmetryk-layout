<script setup>
import InVisit from "./components/InVisit.vue"
import Notifications from "./components/Notifications.vue"
import Bookmarks from "./components/Bookmarks.vue"
import Favorites from "./components/Favorites.vue"
import Settings from "./components/Settings.vue"
import SubFiles from "./components/SubFiles.vue"

</script>

<template>
  <nav class="bg-white">
    <div class="max-w-full px-4 border-b border-gray-300 shadow">
      <div class="flex items-center justify-between h-16">
        <div class="flex items-center">
          <div class="flex-shrink-0">
            <img
                class="h-8 w-8"
                src="https://tailwindui.com/img/logos/workflow-mark-indigo-400.svg"
                alt="Workflow logo"
            >
          </div>
        </div>
        <div class="flex">
          <InVisit/>
          <Notifications/>
          <SubFiles/>
          <Bookmarks/>
          <Favorites/>
          <Settings/>
        </div>
      </div>
    </div>
  </nav>
</template>
