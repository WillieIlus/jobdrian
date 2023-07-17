<template>
  <div class="p-2">
    <NuxtLink :to="logo.NuxtLink.to">
      <img :src="logo.imageUrl" :alt="logo.name" class="h-8 w-auto">
    </NuxtLink>
  </div>
  <div class="p-2">
    <h1 class="text-2xl font-bold">{{ logo.name }}</h1>
  </div>
</template>
  
<script setup>
const logo = {
  name: 'Job Board',
  NuxtLink: { to: '/' },
  imageUrl: 'https://tailwindui.com/img/logos/workflow-mark-indigo-500.svg',
}
</script>
  