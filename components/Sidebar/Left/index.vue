<template>
  <div class="flex flex-col gap-2">
    <div
      class="p-2 w-min rounded-full cursor-pointer transition-colors duration-200 hover:bg-blue-100 dark:hover:bg-gray-800">
      <NuxtLink to="/" class="flex items-center justify-center">
        <LogoTwitter class="w-8 h-8 text-dim-50 dark:text-white" />
      </NuxtLink>
    </div>
    <nav class="flex flex-col gap-2">
      <SidebarLeftTab v-for="item in navigationItems" :key="item.name" :to="item.to">
        <template v-slot:icon>
          <Icon :name="item.icon" class="w-6 h-6" />
        </template>
        <template v-slot:name>
          {{ item.name }}
        </template>
      </SidebarLeftTab>
    </nav>
  </div>
</template>

<script setup lang="ts">
interface NavigationItem {
  name: string
  to: string
  icon: string
}

const navigationItems: NavigationItem[] = [
  { name: 'Home', to: '/', icon: 'lucide:home' },
  { name: 'Explore', to: '/explore', icon: 'lucide:search' },
  { name: 'Notifications', to: '/notifications', icon: 'lucide:bell' },
  { name: 'Messages', to: '/messages', icon: 'lucide:message-circle' },
  { name: 'Profile', to: '/profile', icon: 'lucide:user' }
]
</script>
