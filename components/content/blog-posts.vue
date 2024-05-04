<script setup lang="ts">
import {useAsyncData} from "#app";

const route = useRoute()
const { data: posts } = await useAsyncData(
    'blog-list',
    () => queryContent('/')
        .where({ _path : { $ne: '/blog' } })
        .only(['_path', 'title'])
        .find()
)
</script>

<template>
  <div>
    <section class="not-prose">
      <ul>
        <li v-for="post in posts" :key="post._path">
          <NuxtLink :to="post._path">{{ post.title }}</NuxtLink>
        </li>
      </ul>
    </section>
  </div>
</template>

<style scoped>

</style>