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

      <div class="bg-gray-50 dark:bg-gray-900 min-h-screen">
        <section class="px-6 py-20">
          <div class="max-w-5xl mx-auto">

            <h1 class="text-3xl font-bold text-center mb-14">
              💼 Work Experience
            </h1>

            <div class="space-y-8">
              <div v-for="(job, index) in workExperience" :key="index" class="bg-white rounded-2xl p-6 dark:bg-gray-900 dark:text-white transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110">
                <h2 class="text-2xl font-semibold">{{ job.title }}</h2>
                <p class="text-gray-700 dark:text-gray-500 mt-1">{{ job.company }}</p>
                <p class="text-sm text-gray-700 dark:text-gray-500 mt-1">{{ job.date }}</p>
                <p class="mt-4 text-gray-400">{{ job.description }}</p>
              </div>
            </div>

          </div>
        </section>
      </div>
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

const workExperience = [
  {
    date: 'August 2025 – December 2025',
    title: 'Junior Web Developer',
    company: 'Freelance',
    description: 'Assisted in building responsive web pages using HTML, CSS, and JavaScript. Collaborated with the design team to implement UI components and tested features for functionality and usability.'
  },
  {
    date: 'September 2025 – November 2025',
    title: 'Freelance Web Developer',
    company: 'Self-Employed',
    description: 'Designed and developed personal and client websites, focusing on responsive layouts, clean UI/UX, and modern web technologies including Vue.js and Tailwind CSS.'
  }
]
</script>