<script setup lang="ts">
const route = useRoute()
</script>

<template>
  <div>
    <h1>We are inside a blog.</h1>
    <p>Post id is: {{ route.params.id }}</p>
    <p>Current route: {{ route.path }}</p>
  </div>
</template>

<style scoped>

</style>