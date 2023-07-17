<template>
  <div class="p-2" v-if="isUserLoggedIn">
    <div class="flex items-center relative">
      <img :src="user.imageUrl" :alt="user.name" class="h-8 w-8 rounded-full cursor-pointer" @click="toggleDropdown">
      <div class="ml-2">
        <span class="font-bold">{{ user.name }}</span>
        <span class="text-sm hidden">{{ user.email }}</span>
      </div>
      <div class="absolute right-0 mt-2 w-40 bg-white rounded-lg shadow-lg" v-if="dropdownOpen">
        <div class="py-2 px-4" v-for="item in userNavItems" :key="item.name">
          <NuxtLink :to="item.NuxtLink.to" :class="[item.current ? 'text-white' : 'text-gray-800', 'block py-2 hover:bg-indigo-800 hover:text-white px-4']">
            {{ item.name }}
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
  <div class="p-2" v-else>
    <NuxtLink to="/login" class="text-white hover:cursor-pointer hover:font-bold underline py-3 px-10">
      Login
    </NuxtLink>
  </div>
  <div class="p-2">
    <NuxtLink to="/register" class="text-white hover:cursor-pointer hover:font-bold underline py-3 px-10">
      Register
    </NuxtLink>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { HomeIcon, MagnifyingGlassIcon, BuildingOfficeIcon, RectangleGroupIcon, MapPinIcon } from '@heroicons/vue/24/outline'

const route = useRoute()
const dropdownOpen = ref(false)

const userNavItems = [
  { name: 'Your Profile', NuxtLink: { to: '/profile' }, current: route.name.includes('profile') },
  { name: 'Settings', NuxtLink: { to: '/settings' }, current: route.name.includes('settings') },
  { name: 'Logout', NuxtLink: { to: '/logout' }, current: route.name.includes('logout') },
]

const user = {
  name: 'John Doe',
  email: 'john@example.com',
  imageUrl: 'https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80',
}

const isUserLoggedIn = true;

function toggleDropdown() {
  dropdownOpen.value = !dropdownOpen.value
}
</script>
