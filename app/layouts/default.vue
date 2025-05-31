<template>
  <div class="layout-container">
    <main class="h-[100%] mt-4">
      <slot />
    </main>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.layout-container {
  height: calc(100vh - 4rem);
  background-color: var(--ui-bg);
}
</style>
