<template>
  <CardBase class="flex mx-auto">
    <div class="flex items-center py-2 w-full flex-grow">
      <FormBase class="mx-3 " /><FormBase class="mx-3 " /><FormBase class="mx-3 " /><FormBase class="mx-3 " />
      <ButtonGreen class="flex items-center" ><MagnifyingGlassIcon class="mr-1 h-5 w-5" /> Search</ButtonGreen>
    </div>
  </CardBase>
</template>
  
<script setup>
import { MagnifyingGlassIcon } from '@heroicons/vue/24/outline'
</script>
