<script setup lang="ts">
// definePageMeta({
//   layout: 'another'
// })

// function enableCustomLayout() {
//   setPageLayout('another')
// }
const route = useRoute()
</script>

<template>
  <div>
    <h1>This page is about me.</h1>
    <p>Current route: {{ route.path }}</p>
  </div>
  <!--    <div>-->
  <!--      <button @click="enableCustomLayout">enableCustomLayout</button>-->
  <!--    </div>-->
</template>

<style scoped>

</style>