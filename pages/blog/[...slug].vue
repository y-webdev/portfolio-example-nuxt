<script setup lang="ts">
const route = useRoute()
console.log('slug: ', route.params.slug)
</script>

<template>
  <article>
    <ContentDoc />
  </article>
</template>

<style scoped>

</style>