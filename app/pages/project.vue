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
        <div>
          <p class="text-5xl font-bold text-center pt-20">My Sample Projects</p>
          <p class="text-xl text-center text-gray-600 dark:text-gray-400 mt-10">These projects demonstrate my hands-on
            experience with web development using Vue.js, Tailwind CSS, Node.js, and Firebase. Each project showcases
            clean
            code, responsive UI, and real-world functionality, reflecting my growth as a junior developer.</p>
        </div>

        <div class="relative p-5">
          <div>
            <h3 class="text-3xl text-center font-semibold mt-20">Travel Booking</h3>
            <UCarousel v-slot="{ item, index }" loop dots arrows auto-scroll :items="sample" class="mt-10" :ui="{ item: 'basis-1/3' }">
              <img :src="item" width="320" height="234" class="rounded-lg" @click="openImage(sample, index)">
            </UCarousel>
          </div>

          <div>
            <h3 class="text-3xl text-center font-semibold mt-20">Point of sale (POS)</h3>
            <UCarousel v-slot="{ item, index }" loop dots arrows auto-scroll :items="sample2" class="mt-10" :ui="{ item: 'basis-1/3' }">
              <img :src="item" width="320" height="234" class="rounded-lg" @click="openImage(sample2, index)">
            </UCarousel>
          </div>

          <div>
            <h3 class="text-3xl text-center font-semibold mt-20">Online Bank</h3>
            <UCarousel v-slot="{ item, index }" loop dots arrows auto-scroll :items="sample3" class="mt-10" :ui="{ item: 'basis-1/3' }">
              <img :src="item" width="320" height="234" class="rounded-lg" @click="openImage(sample3, index)">
            </UCarousel>
          </div>

          <div v-if="focusedImage" class="fixed inset-0 bg-black/80 flex items-center justify-center z-50" @click.self="closeImage">

            <UButton class="absolute left-5 text-white text-4xl bg-transparent hover:bg-white/50" @click.stop="prevImage">
              ‹
            </UButton>

            <img :src="focusedImage" class="max-w-[90%] max-h-[90%] rounded-xl shadow-2xl animate-zoom">

            <UButton class="absolute right-5 text-white text-4xl bg-transparent hover:bg-white/50" @click.stop="nextImage">
              ›
            </UButton>

            <UButton class="absolute top-5 right-5 text-white text-2xl bg-transparent hover:bg-white/50" @click="closeImage">
              ✕
            </UButton>
          </div>
        </div>
      </UContainer>
    </div>
  </div>
</template>

<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui'
import { ref } from 'vue'

const items = ref<NavigationMenuItem[][]>([
  [
    {
      class: ' transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-110 cursor-pointer',
      label: 'Home',
      icon: 'i-lucide-home',
      to: '/'
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

const sample = [
  '/images/sample.jpg',
  '/images/sample2.jpg',
  '/images/sample3.jpg',
  '/images/sample4.jpg'
]

const sample2 = [
  '/images/pos.jpg',
  '/images/pos2.jpg',
  '/images/pos3.jpg',
  '/images/pos4.jpg'
]

const sample3 = [
  '/images/soft.jpg',
  '/images/soft2.jpg',
  '/images/soft3.jpg',
  '/images/soft4.jpg',
  '/images/soft5.jpg',
  '/images/soft6.jpg',
  '/images/soft7.jpg'
]

const focusedImage = ref<string | null>(null)
const currentList = ref<string[]>([])
const currentIndex = ref<number>(0)

const openImage = (list: string[], index: number) => {
  const img = list[index]
  if (!img) return

  currentList.value = list
  currentIndex.value = index
  focusedImage.value = img
}


const nextImage = () => {
  if (!currentList.value.length) return

  currentIndex.value =
    (currentIndex.value + 1) % currentList.value.length

  focusedImage.value = currentList.value[currentIndex.value] ?? null
}

const prevImage = () => {
  if (!currentList.value.length) return

  currentIndex.value =
    (currentIndex.value - 1 + currentList.value.length) %
    currentList.value.length

  focusedImage.value = currentList.value[currentIndex.value] ?? null
}

const closeImage = () => {
  focusedImage.value = null
}
</script>