<script setup lang="ts">
const route = useRoute()
console.log('slug: ', route.params.slug)
</script>

<template>
  <article class="prose dark:prose-invert prose-pre:bg-white dark:prose-pre:bg-gray-700 prose-pre:text-gray-700 dark:text-gray-300">
    <ContentDoc />
  </article>
</template>

<style scoped>

</style>