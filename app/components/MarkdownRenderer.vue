<template>
  <MDC :value="content" class="markdown-content" />
</template>

<script setup lang="ts">
defineProps<{ content: string }>();
</script>

<style scoped>
.markdown-content {
  font-size: 1rem;
}
</style>
