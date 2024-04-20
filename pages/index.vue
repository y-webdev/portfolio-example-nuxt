<script setup lang="ts">
useSeoMeta({
  title: 'Main Page',
  description: 'This is main page',
  ogTitle: 'Main Page',
  ogDescription: 'This is main page',
  ogImage: '[og:image]',
  ogUrl: '[og:url]',
  twitterTitle: 'Main Page',
  twitterDescription: 'This is main page',
  twitterImage: '[twitter:image]',
  twitterCard: 'summary'
})

useHead({
  htmlAttrs: {
    lang: 'en'
  },
  link: [
    {
      rel: 'icon',
      type: 'image/png',
      href: '/favicon.ico'
    }
  ]
})

const route = useRoute()
</script>

<template>
  <div>
    <h1>Hello from main page!</h1>
    <p>Current route: {{ route.path }}</p>
  </div>
</template>
