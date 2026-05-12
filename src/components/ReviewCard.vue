<template>
  <article
    class="rounded-lg shadow-sm transition-shadow duration-200 hover:shadow-md bg-gray-primary text-blue-dark"
  >
    <header class="mb-4 p-4 bg-orange-primary rounded-t-lg">
      <h3 class="text-lg font-semibold">{{ name }}</h3>
    </header>

    <p class="p-4 text-md leading-6">{{ comment }}</p>
  </article>
</template>

<script setup lang="ts">
const props = defineProps<{
  name: string
  comment: string
}>()
</script>
