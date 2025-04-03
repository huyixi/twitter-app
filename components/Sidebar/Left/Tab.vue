<template>
  <NuxtLink :to="to"
    class="flex items-center w-fit p-2 h-12 rounded-full hover:bg-gray-100 dark:hover:bg-dim-200 transition duration-200">
    <div class="flex items-center text-dark text-lg dark:text-white">
      <slot name="icon"></slot>
    </div>
    <div class="hidden xl:block ml-4 text-lg text-dark dark:text-white">
      <slot name="name"></slot>
    </div>
  </NuxtLink>
</template>

<script setup>
defineProps({
  to: {
    type: String,
    default: '/'
  }
})
</script>
