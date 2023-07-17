<template>
  <CardBase>
    <div v-for="category in categories" :key="category.id" class="flex items-center">
      <input type="checkbox" class="mr-2" />
      <NuxtLink :to="`/categories/${slug}`" class=" flex-grow text-blue-500 hover:underline">{{ category.name }}</NuxtLink>
      <span class="text-sm text-gray-500">({{ category.job_count }})</span>
    </div>
  </CardBase>
</template>

<script setup>
const { categories } = defineProps({
  categories: {
    type: Array,
    required: true
  }
})

</script>  
