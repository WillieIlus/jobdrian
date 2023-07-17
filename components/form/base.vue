<template>
<form class="w-full max-w-lg " @submit.prevent="submit">
    <input type="text" class="shadow appearance-none rounded w-full py-3 px-3 text-zink-700 leading-tight focus:outline-none focus:shadow-outline border-zinc-300 border-2 text-indigo-800" placeholder="Search">
    <slot></slot>
</form>
</template>

<script>
const submit = null
</script>