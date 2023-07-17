<template>
  <div class="bg-indigo-600 text-white p-4 h-96">
    <div class="flex justify-between mx-auto container flex-col text-center">

      <h1 class="text-6xl font-sans font-semibold tracking-tight pt-40 mb-4">
        <!-- display the currently active item name/ -->
        <!-- display the current route.name here -->
        <div v-for="item in breadcrumbs" :key="item.name">
          <span v-if="item.current">{{ item.name }}</span>
        </div>
      </h1>
      <div class="flex items-center justify-center mt-4">
        <div class="text-indigo-200 hover:text-white hover:cursor-pointer flex items-center">
          <NuxtLink :to="item.NuxtLink.to" v-for="(item, index) in breadcrumbs" :key="index" :class="[
            item.current ? 'text-emerald-500 font-bold' : 'text-indigo-200 hover:text-white hover:cursor-pointer',
            'flex items-center'
          ]">
            <span class="text-sm">{{ item.name }}</span>
            <ChevronRightIcon class="w-5 h-5 text-indigo-200" />
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>


<script setup>
import { ChevronRightIcon } from '@heroicons/vue/24/outline'

const route = useRoute()
const breadcrumbs = computed(() => {
  const breadcrumbs = [{ name: 'Home', NuxtLink: { to: '/' }, current: route.path === '/' }]
  const paths = route.path.split('/').filter(Boolean)
  paths.reduce((acc, path) => {
    acc += `/${path}`
    breadcrumbs.push({
      name: path,
      NuxtLink: { to: acc },
      current: acc === route.path
    })
    return acc
  }, '')
  return breadcrumbs
})

</script>

