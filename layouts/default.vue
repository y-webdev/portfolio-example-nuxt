<script setup lang="ts">
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
  <div class="container mx-auto max-w-4xl">
    <header class="flex items-center justify-between mt-5">
      <div class="flex items-center space-x-12">
        <div>
          <NuxtLink to="/" class="text-2xl font-semibold p-2 hover:bg-gray-200">Yanni Pavlov</NuxtLink>
        </div>
        <Menu/>
      </div>
      <ClientOnly>
        <ColorModeSelector />
      </ClientOnly>
    </header>
    <main class="p-2 mt-10">
      <slot />
    </main>
  </div>
</template>

<style>
body {
  font-family: 'Roboto', sans-serif;
  @apply
  bg-white
  dark:bg-gray-800
  text-gray-700
  dark:text-gray-300
}
</style>