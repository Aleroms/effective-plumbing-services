<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui'

useHead({
  meta: [{ name: 'viewport', content: 'width=device-width, initial-scale=1' }],
  link: [{ rel: 'icon', href: '/favicon.ico' }],
  htmlAttrs: {
    lang: 'en'
  }
})

const title = 'Effective Plumbing Services'
const title2 = title + ' | South Orange County Plumber (C-36 Licensed)'
const description
  = 'Licensed C-36 plumbing contractor in South Orange County offering residential and emergency plumbing, drain cleaning, water heater & sewer services.'

const items = computed<NavigationMenuItem[]>(() => [
  {
    label: 'Services',
    to: '/services',
    icon: 'i-lucide-wrench'
  },
  {
    label: 'About',
    to: '/about',
    icon: 'i-lucide-users'
  },
  {
    label: 'Gallery',
    to: '/gallery',
    icon: 'i-lucide-gallery-vertical-end'
  },
  {
    label: 'Contact',
    to: '/contact',
    icon: 'i-lucide-phone'
  }
])

useSeoMeta({
  title: title,
  description:
    description,
  ogTitle: title2,
  ogDescription:
    description,
  ogType: 'website',
  twitterCard: 'summary_large_image',
  twitterTitle: title2,
  twitterImage: 'https://lh3.googleusercontent.com/p/AF1QipPl6NGfpF3Wt1Xrz_OCPCpdydMAXDsMT-5I06ec=s680-w680-h510-rw',
  twitterDescription:
    description,
  ogUrl: 'https://effectiveplumbingservices.com',
  ogImage: 'https://lh3.googleusercontent.com/p/AF1QipPl6NGfpF3Wt1Xrz_OCPCpdydMAXDsMT-5I06ec=s680-w680-h510-rw'
})
</script>

<template>
  <UApp>
    <UHeader mode="slideover">
      <template #title>
        Effective Plumbing Services
      </template>

      <template #right>
        <UNavigationMenu
          :items="items"
          class="hidden lg:flex"
        />
      </template>

      <template #body>
        <UNavigationMenu
          :items="items"
          orientation="vertical"
        />
      </template>
    </UHeader>

    <UMain>
      <NuxtPage />
    </UMain>

    <USeparator icon="i-simple-icons-nuxtdotjs" />

    <UFooter>
      <template #left>
        <p class="text-sm text-muted">
          Built with Nuxt UI • © {{ new Date().getFullYear() }}
        </p>
      </template>

      <template #right>
        <UButton
          to="https://github.com/nuxt-ui-templates/starter"
          target="_blank"
          icon="i-simple-icons-github"
          aria-label="GitHub"
          color="neutral"
          variant="ghost"
        />
      </template>
    </UFooter>
  </UApp>
</template>
