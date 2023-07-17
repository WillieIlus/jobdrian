<template>
    <CardBase>
      <div v-for="location in locations" :key="location.id" class="flex items-center">
        <input type="radio" class="mr-2" />
        <NuxtLink :to="`/locations/${slug}`" class="flex-grow text-blue-500 hover:underline">{{ location.name }}</NuxtLink>
        <span class="text-sm text-gray-500">({{ location.job_count }})</span>
      </div>
    </CardBase>
  </template>
  <script setup>
  const { locations } = defineProps({
    locations: {
      type: Array,
      required: true,
    },
  });
  </script>
  
<!-- <script setup>
const { locations } = defineProps({
    locations: {
        type: Array,
        required: true
    }
})
</script> -->
