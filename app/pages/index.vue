<template>
  <div>
    <NuxtPage />
    <div>
      <UHeader title="" toggle-side="right">
        <UNavigationMenu :items="items" class="w-full justify-center" :ui="{label: 'active:text-blue-500'}" />

        <template #right>
          <UColorModeButton />
        </template>

        <template #body>
          <UNavigationMenu :items="items" orientation="vertical" class="-mx-2.5 shadow-lg" />
        </template>
      </UHeader>
      </div>
    <div class="bg-gray-50 dark:bg-gray-900">
      <UContainer>
        <div class="flex justify-between">
          <div class="min-h-screen">
            <p class="w-full text-lg ms-5 sm:ms-10 md:ms-15 sm:text-2xl md:text-3xl mt-20 sm:mt-40 text-gray-500 dark:text-white">Hi, I'm Kiraly</p>
            <p class="w-full text-xl sm:text-3xl md:text-5xl font-bold ms-5 sm:ms-10 md:ms-15 mt-2 sm:mt-5">Junior Web</p>
            <p class="w-full text-xl sm:text-3xl md:text-5xl font-bold ms-5 sm:ms-10 md:ms-15">Developer</p>
            <p class="w-full text-xl ms-5 sm:ms-10 md:ms-15 mt-2 text-gray-500 dark:text-white">I build responsive website and web applications.</p>
            <div class="flex">
              <UButton class="mt-10 sm:mt-6 ms-5 sm:ms-15 md:ms-20 p-1 sm:p-4 text-xs sm:text-sm rounded-xl bg-blue-500 hover:bg-blue-100">View My Project</UButton>
              <UButton class="mt-10 sm:mt-6 ms-2 sm:ms-10 md:ms-5 p-1 sm:p-4 text-xs sm:text-sm rounded-xl bg-gray-400 hover:bg-gray-300"><UIcon name="i-lucide-send" />Contact Me</UButton>
            </div>
          </div>
          
          <div class="w-80 h-50 sm:w-70 md:w-100 sm:h-70 md:h-100 rounded-2xl bg-blue-50 dark:bg-gray-800 overflow-hidden mt-15 ms-10">
            <img src="/assets/formal1.png" alt="picture" class="object-cover w-full h-full">
          </div>
        </div>
      </UContainer>
    </div>
  </div>
</template>

<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui'

const items = ref<NavigationMenuItem[][]>([
  [
    {
      label: 'Home',
      icon: 'i-lucide-home',
      to: '',
      active: true
    },
    {
      label: 'About me',
      icon: 'i-lucide-user-round',
      to: ''
    },
    {
      label: 'Education',
      icon: 'i-lucide-book',
      to: '',
    },
    {
      label: 'Work experience',
      icon: 'i-lucide-briefcase-business',
      to: ''
    },
    {
      label: 'Project',
      icon: 'i-lucide-layers',
      to: ''
    },
    {
      label: 'Contact',
      icon: 'i-lucide-send',
      to: ''
    }
  ],
  [
    {
      label: 'GitHub',
      icon: 'i-simple-icons-github',
      badge: 'NEW',
      to: 'https://github.com/sukehiro27',
      target: '_blank'
    }
  ]
])
</script>