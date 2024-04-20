<script setup lang="ts">
import Menu from "~/components/menu.vue";
useHead({
  titleTemplate: '%s - Yanni Pavlov',
  link: [
    {
      rel: 'preconnect',
      href: 'https://fonts.googleapis.com'
    },
    {
      rel: 'stylesheet',
      href: 'https://fonts.googleapis.com/css2?family=Roboto&display=swap',
      crossorigin: ''
    }
  ]
})
</script>

<template>
  <div class="container mx-auto max-w-2xl">
    <header class="flex items-center justify-between mt-5">
      <div>
        <NuxtLink to="/" class="text-2xl font-semibold p-2 hover:bg-gray-200">Yanni Pavlov</NuxtLink>
      </div>
      <Menu/>
    </header>
    <main class="p-2">
      <slot />
    </main>
  </div>
</template>

<style>
body {
  font-family: 'Roboto', sans-serif;
}
</style>