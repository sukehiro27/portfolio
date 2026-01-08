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
        <div class="flex justify-between ">
          <div>
            <p
              class="w-full text-lg ms-5 sm:ms-10 md:ms-15 sm:text-2xl md:text-3xl mt-20 sm:mt-40 text-gray-500 dark:text-white">
              Hi, I'm Kiraly</p>
            <p class="w-full text-xl sm:text-3xl md:text-5xl font-bold ms-5 sm:ms-10 md:ms-15 mt-2 sm:mt-5">Junior Web
            </p>
            <p class="w-full text-xl sm:text-3xl md:text-5xl font-bold ms-5 sm:ms-10 md:ms-15">Developer</p>
            <p class="w-full text-xl ms-5 sm:ms-10 md:ms-15 mt-2 text-gray-500 dark:text-white">I build responsive
              website
              and web applications.</p>
            <div class="flex">
              <UButton
                class="cursor-pointer mt-10 sm:mt-6 ms-5 sm:ms-15 md:ms-20 p-1 sm:p-4 text-xs sm:text-sm rounded-xl transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110 bg-blue-500 hover:bg-blue-300 shadow-lg dark:shadow-xl">
                View My Project</UButton>
              <UButton
                class="cursor-pointer mt-10 sm:mt-6 ms-2 sm:ms-10 md:ms-5 p-1 sm:p-4 text-xs sm:text-sm rounded-xl transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110 bg-gray-400 hover:bg-gray-300 shadow-lg dark:shadow-xl">
                <UIcon name="i-lucide-send" />Contact Me
              </UButton>
            </div>
          </div>

          <div class="w-80 h-50 sm:w-70 md:w-90 sm:h-70 md:h-90 rounded-2xl bg-blue-50 dark:bg-gray-800 overflow-hidden mt-17 ms-10">
            <img src="/assets/formal1.png" alt="picture" class="object-cover w-full h-full transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110">
          </div>
        </div>

        <div class="mt-35 flex-col-2 sm:flex">
          <p class="font-bold text-xl ms-5 sm:ms-10 md:ms-15">Skills</p>
          <div class="skill-card opacity-0 translate-y-6 transition-all duration-700 ease-out">
            <UCard class="w-70 ms-5 mt-15 h-70 hover:-translate-y-1 hover:scale-110 transition">
              <p class="font-bold text-xl text-center">Front-end</p>
              <USeparator />
              <section class="mt-5">
                <p class="font-semibold">HTML</p>
                <p class="font-semibold">CSS</p>
                <p class="font-semibold">Javascript</p>
              </section>
            </UCard>
          </div>

          <div class="skill-card opacity-0 translate-y-6 transition-all duration-700 ease-out">
            <UCard class="w-70 ms-5 mt-15 h-70 hover:-translate-y-1 hover:scale-110 transition">
              <p class="font-bold text-xl text-center">Back-end</p>
              <USeparator />
              <section class="mt-5">
                <p class="font-semibold">PHP</p>
                <p class="font-semibold">Firebase</p>
              </section>
            </UCard>
          </div>

          <div class="skill-card opacity-0 translate-y-6 transition-all duration-700 ease-out">
            <UCard class="w-70 ms-5 mt-15 h-70 hover:-translate-y-1 hover:scale-110 transition">
              <p class="font-bold text-xl text-center">Tools</p>
              <USeparator />
              <section class="mt-5">
                <p class="font-semibold">Bootstrap</p>
                <p class="font-semibold">Vue</p>
                <p class="font-semibold">Nuxt js</p>
                <p class="font-semibold">Tailwindcss</p>
              </section>
            </UCard>
          </div>
        </div>
      </UContainer>
    </div>
  </div>
</template>

<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui'
import { onMounted } from 'vue'

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

onMounted(() => {
  const cards = document.querySelectorAll('.skill-card')

  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.remove('opacity-0', 'translate-y-6')
          entry.target.classList.add('opacity-100', 'translate-y-0')
          observer.unobserve(entry.target)
        }
      })
    },
    {
      threshold: 0,
      rootMargin: '0px 0px -150px 0px'
    }
  )

  cards.forEach((card) => observer.observe(card))
})
</script>