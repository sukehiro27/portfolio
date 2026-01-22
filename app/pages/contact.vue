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
    <div class="min-h-screen bg-gray-50 dark:bg-gray-900 text-gray-800 dark:text-gray-100 flex flex-col items-center justify-center px-5 py-20 space-y-12">

  
    <section class="text-center space-y-4">
      <h1 class="text-4xl md:text-5xl font-bold">Let's Connect</h1>
      <p class="text-lg md:text-xl text-gray-600 dark:text-gray-300 max-w-xl mx-auto">
        I’m always open to chat about projects, collaborations, or just say hi!  
        Reach me through any of the platforms below.
      </p>
    </section>

  
    <section class="flex flex-wrap justify-center gap-6 md:gap-8 text-center">
   
      <a href="https://mail.google.com/mail/u/1/#inbox?compose=CllgCJTGmSQKjzwjZnQSCXWFZznFlXkRsNJvJpfXlRfspxdBJmWPpLjjLCzTbZvVBBQTsLvhSQq"  class="flex flex-col items-center justify-center bg-white dark:bg-gray-800 shadow-lg rounded-xl px-8 py-6 w-48 hover:bg-blue-500 hover:text-white transition transform hover:scale-105">
        <svg class="w-10 h-10 mb-2" fill="currentColor" viewBox="0 0 24 24">
          <path d="M2 4h20v16H2V4zm2 2v2l8 5 8-5V6H4zm16 12V9l-8 5-8-5v7h16z"/>
        </svg>
        <span class="font-semibold">Email Me</span>
      </a>
    
      <a href="https://github.com/sukehiro27" target="_blank" class="flex flex-col items-center justify-center bg-white dark:bg-gray-800 shadow-lg rounded-xl px-8 py-6 w-48 hover:bg-gray-900 hover:text-white transition transform hover:scale-105">
        <svg class="w-10 h-10 mb-2" fill="currentColor" viewBox="0 0 24 24">
          <path d="M12 0C5.37 0 0 5.373 0 12c0 5.303 3.438 9.8 8.205 11.387.6.113.82-.26.82-.577v-2.23c-3.338.724-4.033-1.61-4.033-1.61-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.085 1.838 1.238 1.838 1.238 1.07 1.834 2.807 1.304 3.492.997.108-.775.418-1.305.76-1.605-2.665-.3-5.467-1.333-5.467-5.932 0-1.31.467-2.38 1.236-3.22-.124-.303-.536-1.523.117-3.176 0 0 1.008-.322 3.3 1.23a11.5 11.5 0 0 1 3-.404c1.02.005 2.047.138 3 .404 2.29-1.552 3.296-1.23 3.296-1.23.655 1.653.243 2.873.12 3.176.77.84 1.236 1.91 1.236 3.22 0 4.61-2.807 5.628-5.48 5.922.43.37.823 1.096.823 2.21v3.282c0 .32.217.694.825.576C20.565 21.796 24 17.3 24 12c0-6.627-5.373-12-12-12z"/>
        </svg>
        <span class="font-semibold">GitHub</span>
      </a>
    
      <a href="https://www.linkedin.com/in/kiraly-llanda-b984a0368/?originalSubdomain=ph" target="_blank" class="flex flex-col items-center justify-center bg-white dark:bg-gray-800 shadow-lg rounded-xl px-8 py-6 w-48 hover:bg-blue-700 hover:text-white transition transform hover:scale-105">
        <svg class="w-10 h-10 mb-2" fill="currentColor" viewBox="0 0 24 24">
          <path d="M4.98 3.5C4.98 4.88 3.88 6 2.5 6S0 4.88 0 3.5 1.12 1 2.5 1s2.48 1.12 2.48 2.5zM0 8h5v16H0V8zm7.5 0h4.7v2.2h.1c.65-1.2 2.24-2.2 4.6-2.2 4.9 0 5.8 3.2 5.8 7.3V24h-5v-7c0-1.7-.03-3.8-2.3-3.8-2.3 0-2.66 1.8-2.66 3.7V24h-5V8z"/>
        </svg>
        <span class="font-semibold">LinkedIn</span>
      </a>
    
      <a href="https://www.facebook.com/phyongrhap.llanda" target="_blank" class="flex flex-col items-center justify-center bg-white dark:bg-gray-800 shadow-lg rounded-xl px-8 py-6 w-48 hover:bg-blue-600 hover:text-white transition transform hover:scale-105">
        <svg class="w-10 h-10 mb-2" fill="currentColor" viewBox="0 0 24 24">
          <path d="M12 2C6.48 2 2 6.48 2 12c0 4.42 3.22 8.08 7.5 8.88V14H7v-2h2.5v-2c0-2.5 1.5-3.88 3.78-3.88 1.1 0 2.26.2 2.26.2v2.48H13c-1.24 0-1.63.77-1.63 1.55v1.85H15l-.5 2H11v6.88C16.78 20.08 20 16.42 20 12c0-5.52-4.48-10-10-10z"/>
        </svg>
        <span class="font-semibold">Messenger</span>
      </a>
    
      <a href="https://wa.me/09669575979" target="_blank" class="flex flex-col items-center justify-center bg-white dark:bg-gray-800 shadow-lg rounded-xl px-8 py-6 w-48 hover:bg-green-500 hover:text-white transition transform hover:scale-105">
        <svg class="w-10 h-10 mb-2" fill="currentColor" viewBox="0 0 24 24">
          <path d="M20.52 3.48A11.88 11.88 0 0 0 12 0C5.37 0 0 5.37 0 12c0 2.11.55 4.09 1.6 5.85L0 24l6.27-1.64A11.94 11.94 0 0 0 12 24c6.63 0 12-5.37 12-12 0-3.18-1.23-6.17-3.48-8.52zM12 22a10 10 0 0 1-5.1-1.4l-.36-.21-3.73.97.99-3.62-.23-.37A9.99 9.99 0 1 1 12 22z"/>
        </svg>
        <span class="font-semibold">WhatsApp</span>
      </a>

      <a href="https://ph.jobstreet.com/profiles/kiraly-llanda-3gC0nCtpFt" target="_blank" class="flex flex-col items-center justify-center bg-white dark:bg-gray-800 shadow-lg rounded-xl px-8 py-6 w-48 hover:bg-yellow-500 hover:text-white transition transform hover:scale-105">
        <svg class="w-10 h-10 mb-2" fill="currentColor" viewBox="0 0 24 24">
          <path d="M12 0L1.8 6v12l10.2 6 10.2-6V6L12 0zm0 2.18L20.4 7 12 11.82 3.6 7 12 2.18zm0 17.64l-8.4-4.9V8.45l8.4 4.8 8.4-4.8v6.47l-8.4 4.9z"/>
        </svg>
        <span class="font-semibold">JobStreet</span>
      </a>

    </section>
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