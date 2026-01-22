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
        <div class="flex justify-center">
          <h1 class="text-3xl font-bold mt-20 mb-10">
            🎓Education
          </h1>
        </div>

        <UCard class="flex-1">
          <UTimeline :items="edu" class="-p- sm:p-15" />
        </UCard>
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

const edu = ref([
  {
    date: 'Batch 2019-2020',
    title: 'Klayaan National HighSchool (KNHS)',
    description: 'Completed secondary education with a strong foundation, discipline, and teamwork. Developed essential learning skills and interest in technology.',
    icon: 'i-lucide-school'
  },
  {
    date: 'Batch 2020-2022',
    title: 'St. Clare College of Caloocan (SCC)',
    description: 'Completed Senior HighSchool under the ICT strand, gaining foundational knowledge in computer systems, basic programming, and web technologies. Developed problem-solving and technical skills.',
    icon: 'i-lucide-monitor'
  },
  {
    date: '3rd year 2023-Present',
    title: 'Bestlink College of the Philippines (BCP)',
    description: 'Currently a 3rd-year Bachelor of Science in Information Technology student, focusing on web development, programming fundamentals, databases, and system design. Gaining hands-on experience through academic and personal projects.',
    icon: 'i-lucide-graduation-cap'
  },
])
</script>