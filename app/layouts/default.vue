<template>
  <div class="layout-container">
    <AppHeader @toggle-sidebar="isSidebarOpen = !isSidebarOpen" />
    <AppSidebar :is-open="isSidebarOpen" />
    <main
      class="h-[100%] mt-16 transition-all duration-300 ease-in-out"
      :class="{
        'ml-64': isSidebarOpen,
      }"
    >
      <slot />
    </main>
  </div>
</template>

<script setup lang="ts">
const isSidebarOpen = ref(true);
</script>

<style scoped>
.layout-container {
  height: calc(100vh - 4rem);
  background-color: var(--ui-bg);
}
</style>
