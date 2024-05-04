<script setup lang="ts">
const route = useRoute()
console.log('slug: ', route.params.slug)
</script>

<template>
  <article class="prose dark:prose-invert max-w-none prose-pre:bg-white dark:prose-pre:bg-gray-700 prose-pre:text-gray-700 dark:text-gray-300">
    <ContentDoc v-slot="{ doc }">
      {{ doc.body.toc.links }}
      <div class="grid grid-cols-6 gap-16">
        <div :class="{
          'col-span-4': doc.toc,
          'col-span-6': !doc.toc
        }">
          <ContentRenderer :value="doc" />
        </div>
        <div class="col-span-2 not-prose" v-if="doc.toc">
          <aside class="sticky top-8">
            <div class="font-semibold mb-2">
              Table of Contents
            </div>
            <nav>
              <TocLinks :links="doc.body.toc.links"></TocLinks>
            </nav>
          </aside>
        </div>
      </div>
    </ContentDoc>
  </article>
</template>

<style scoped>

</style>