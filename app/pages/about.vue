<template>
  <div>
    <NuxtPage />
    <div>
      <UHeader title="" toggle-side="right">
        <UNavigationMenu :items="items" class="w-full justify-center" :ui="{ label: 'active:text-blue-500' }" />

        <template #right>
          <UColorModeButton />
        </template>

        <template #body>
          <UNavigationMenu :items="items" orientation="vertical" class="-mx-2.5 shadow-lg" />
        </template>
      </UHeader>
    </div>
    <div class="bg-gray-50 dark:bg-gray-900 min-h-screen">
      <UContainer>
        <div class="flex">
          <div class="flex-1 text-left">
            <h1 class="font-bold text-3xl pt-20 mb-5">---About Me---</h1>
            <p class="font-semibold text-2xl">Hi, I'm Kiraly</p>
            <p>I'm a junior wed developer specializing in creating clean and responsive websites.
              I have passion for writing code that is simple yet effective.
            </p>
            <p class="pt-5">I enjoy learning the latest front-end and back-end technologies to build practical web appplications, and continually improve my skills.</p>
          </div>

          <div class="flex-1">
            <div>
              <UCard class="ms-20 mt-35 rounded-xl shadow-lg">
                <UIcon name="i-lucide-user-round" class="w-10 h-10 absolute" />
                <div class="flex flex-col ms-15">
                  <h1 class="text-muted">Full Name</h1>
                  <p class="font-semibold">Kiraly Llanda</p>
                </div>
              </UCard>
            </div>
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
      class: ' transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110 cursor-pointer',
      label: 'Home',
      icon: 'i-lucide-home',
      to: '/',
    },
    {
      class: ' transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110 cursor-pointer',
      label: 'About me',
      icon: 'i-lucide-user-round',
      to: '/about'
    },
    {
      class: ' transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110 cursor-pointer',
      label: 'Education',
      icon: 'i-lucide-book',
      to: '',
    },
    {
      class: ' transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110 cursor-pointer',
      label: 'Work experience',
      icon: 'i-lucide-briefcase-business',
      to: ''
    },
    {
      class: ' transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110 cursor-pointer',
      label: 'Project',
      icon: 'i-lucide-layers',
      to: ''
    },
    {
      class: ' transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110 cursor-pointer',
      label: 'Contact',
      icon: 'i-lucide-send',
      to: ''
    }
  ],
  [
    {
      class: ' transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110 cursor-pointer',
      label: 'GitHub',
      icon: 'i-simple-icons-github',
      badge: 'NEW',
      to: 'https://github.com/sukehiro27',
      target: '_blank'
    }
  ]
])
</script>