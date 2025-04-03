<template>
  <div class="grid grid-cols-12 gap-4 max-w-[1000px] mx-auto">
    <div class="bg-red-100 col-span-3">
      <SidebarLeft />
    </div>
    <main class="bg-yellow-300 col-span-6 max-w-[600px]">
      <slot></slot>
    </main>
    <div class="bg-blue-300 col-span-3">
      <SidebarRight />
    </div>
  </div>
</template>
