<template>
  <div class="p-2" v-for="item in navItems" :key="item.name">
    <NuxtLink :to="item.NuxtLink.to" :class="[
      item.current ? 'bg-indigo-700 hover:bg-indigo-800 text-white round-lg overflow:hidden' : 'text-white hover:cursor-pointer hover:font-bold underline',
      'py-3 px-10'
    ]">
      <item.icon class="w-5 h-5 mr-2 text-white"> icon </item.icon>
      {{ item.name }}
    </NuxtLink>
  </div>
</template>
  
<script setup>
import { HomeIcon, MagnifyingGlassIcon, BuildingOfficeIcon, RectangleGroupIcon, MapPinIcon } from '@heroicons/vue/24/outline'

const route = useRoute()
const navItems = [
  { name: 'Home', icon: HomeIcon, NuxtLink: { to: '/' }, current: route.name === 'index' },
  { name: 'Jobs', icon: MagnifyingGlassIcon, NuxtLink: { to: '/jobs' }, current: route.name.includes('jobs') },
  { name: 'Companies', icon: BuildingOfficeIcon, NuxtLink: { to: '/companies' }, current: route.name.includes('companies') },
  { name: 'Categories', icon: RectangleGroupIcon, NuxtLink: { to: '/categories' }, current: route.name.includes('categories') },
  { name: 'Location', icon: MapPinIcon, NuxtLink: { to: '/location' }, current: route.name.includes('location') },
]
</script>
  