<template>
  <CardBase v-for="job in jobs" :key="job.slug">
    <div class="flex">
      <div class="w-1/4">
        <img src="https://via.placeholder.com/150" alt="logo" />
      </div>
      <div class="w-3/4">
        <div class="flex justify-between items-center">
          <div>
            <h2 class="text-xl font-bold ">
              <NuxtLink :to="`/jobs/${job.slug}`">{{ job.title }}</NuxtLink>
            </h2>
            <div class="flex items-center">
              <span class="text-sm text-gray-500 flex items-center mx-2">
                <RectangleGroupIcon class="h-5 w-5 mr-1" />
                {{ job.category }}
              </span>
              <span class="text-sm text-gray-500 flex items-center mx-2">
                <MapPinIcon class="h-5 w-5 mr-1" />
                {{ job.location }}
              </span>
            </div>
          </div>
          <div class="mt-4">
            <ButtonGreen class="flex items-center">
              Apply
              <DocumentArrowUpIcon class="h-5 w-5 ml-1" />
            </ButtonGreen>
            <div class="text-sm text-gray-500">{{ job.timesince }}</div>
          </div>
        </div>
        <div class="mt-4">
          <p class="text-sm text-gray-500">{{ job.description }}</p>
        </div>
        <div class="mt-4 flex items-center">
          <span class="text-sm text-gray-500 flex items-center mx-2">
            <EyeIcon class="h-5 w-5 mr-1" />
            {{ job.view_count }}
          </span>
          <span class="text-sm text-gray-500 flex items-center mx-2">
            <DocumentCheckIcon class="h-5 w-5 mr-1" />
            {{ job.apply_count }}
          </span>
        </div>
      </div>
    </div>
  </CardBase>
</template>

<!-- Rest of your script setup goes here -->

  

<script setup>
import { DocumentArrowUpIcon, DocumentCheckIcon, RectangleGroupIcon, MapPinIcon, EyeIcon } from '@heroicons/vue/24/outline'

const { jobs } = defineProps({
  jobs: {
    type: Array,
    required: true
  }
})
</script>