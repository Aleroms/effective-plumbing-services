<template>
  <div>
    <!-- header  -->
    <UPageSection
      title="Hi, i'm George - Your Local Plumbing Expert"
      orientation="horizontal"
      description="We have over 20 years of hands-on experience, are a C-36 licensed plumbing contractor proudly serving South Orange County with honest, dependable service."
    >
      <div class="flex justify-center">
        <NuxtImg
          src="aboutPic.jpg"
          format="webp"
          width="400"
          height="350"
          class="rounded-lg"
        />
      </div>
    </UPageSection>
    <UContainer>
      <USeparator type="dashed" />
      <UPageSection
        id="features"
        title="Our Values"
        :features="[{
          icon: 'i-lucide-handshake',
          title: 'Honest Work, Fair Pricing',
          description: 'We believe in transparency — clear communication, no hidden fees, and reliable service you can trust from start to finish.'
        }, {
          icon: 'i-lucide-users',
          title: 'Community Commitment',
          description: 'As a local, family-owned business, we value our neighbors and treat every customer like part of the Effective Plumbing Service family. Your trust keeps us proud to serve Orange County and beyond. '
        }, {
          icon: 'i-lucide-home',
          title: 'Safety First',
          description: ' Every service we perform is focused on protecting your home and family. From cleanings to repairs, we follow strict safety standards and never cut corners. '
        }]"
      />
      <div class="flex justify-center">
        <UPageCTA
          title="Let's Get Your Plumbing Done Right"
          variant="soft"
          :links="links"
          class="w-250 mb-30"
          description="If you're dealing with a plumbing issue or need an estimate, send me a message. I'll get back to you as soon as possible."
        />
      </div>
    </UContainer>

    <!-- <USeparator icon="i-simple-icons-nuxtdotjs" /> -->
  </div>
</template>

<script lang="ts" setup>
import type { ButtonProps } from '@nuxt/ui'

const links = ref<ButtonProps[]>([
  {
    label: 'Contact',
    to: '/contact',
    color: 'neutral',
    variant: 'subtle',
    trailingIcon: 'i-lucide-arrow-right'
  }
])
</script>

<style>

</style>
