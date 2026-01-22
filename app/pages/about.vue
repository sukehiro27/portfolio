<template>
  <div>
    <NuxtPage />
    <div>
      <UHeader title="" toggle-side="right">
        <UNavigationMenu :items="items" color="secondary" class="w-full justify-center" />

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
        <div class="grid-cols-2 sm:flex">
          <div class="flex-1 text-left">
            <h1 class="font-bold text-3xl pt-40 mb-15">---About Me---</h1>
            <p class="font-semibold text-2xl">Hi, I'm Kiraly</p>
            <p>I'm a junior web developer specializing in creating clean and responsive websites.
              I have passion for writing code that is simple yet effective.
            </p>
            <p class="pt-5">I enjoy learning the latest front-end and back-end technologies to build practical web appplications, and continually improve my skills.</p>
          </div>

          <div class="flex-1 -ms- sm:ms-20">
            <div class="transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110">
              <UCard class="mt-35 rounded-xl shadow-lg">
                <UIcon name="i-lucide-user-round" class="w-10 h-10 absolute" />
                <div class="flex flex-col ms-15">
                  <h1 class="text-muted">Full Name</h1>
                  <p class="font-semibold">Kiraly Llanda</p>
                </div>
              </UCard>
            </div>

            <div class="transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110">
              <UCard class="mt-3 rounded-xl shadow-lg">
                <UIcon name="i-lucide-code" class="w-10 h-10 absolute" />
                <div class="flex flex-col ms-15">
                  <h1 class="text-muted">Role</h1>
                  <p class="font-semibold">Junior Web Developer</p>
                </div>
              </UCard>
            </div>

            <div class="transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110">
              <UCard class="mt-3 rounded-xl shadow-lg">
                <UIcon name="i-lucide-map-pin" class="w-10 h-10 absolute" />
                <div class="flex flex-col ms-15">
                  <h1 class="text-muted">Location</h1>
                  <p class="font-semibold">Philippines</p>
                </div>
              </UCard>
            </div>

            <div class="transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110">
              <UCard class="mt-3 rounded-xl shadow-lg">
                <UIcon name="i-lucide-briefcase-business" class="w-10 h-10 absolute" />
                <div class="flex flex-col ms-15">
                  <h1 class="text-muted">Experience</h1>
                  <p class="font-semibold">Entry Level</p>
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
      to: '/educations',
    },
    {
      class: ' transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110 cursor-pointer',
      label: 'Work experience',
      icon: 'i-lucide-briefcase-business',
      to: '/experience'
    },
    {
      class: ' transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110 cursor-pointer',
      label: 'Project',
      icon: 'i-lucide-layers',
      to: '/project'
    },
    {
      class: ' transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110 cursor-pointer',
      label: 'Contact',
      icon: 'i-lucide-send',
      to: '/contact'
    }
  ],
  [
    {
      class: ' transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110 cursor-pointer',
      label: 'GitHub',
      icon: 'i-simple-icons-github',
      badge: 'Click',
      to: 'https://github.com/sukehiro27',
      target: '_blank'
    }
  ]
])
</script>