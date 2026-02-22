<template>
  <div>
    <ImageHero
      title="Our Services"
      image-path="/services_bg.jpg"
    />
    <!-- INTRODUCTION TO COMPANY  -->
    <UPageSection
      orientation="horizontal"
      title="Effective Plumbing Services LLC"
      headline="Servicing Orange County since 2001"
      description="With decades of hands-on experience, we help homeowners avoid costly damage and unexpected repairs."
    >
      <template #default>
        <NuxtImg
          src="serviceArea.png"
          alt="Mission Viejo Service Area"
          class="w-full max-w-md"
          format="webp"
        />
      </template>
    </UPageSection>
    <UPageSection
      title="Professional Plumbing Solutions You Can Trust"
      description="From routine maintenance to emergency repairs, our licensed plumbers deliver reliable, high-quality service for residential and commercial properties. We handle everything from leak detection and pipe repairs to water heater installations and drain cleaning—all backed by our satisfaction guarantee."
      :features="services"
    />
    <UPageSection
      title="Frequently Asked Questions"
      description="Got questions? We've got answers. Browse our most common plumbing inquiries below."
    >
      <PlumbingFaq />
      <UPageCTA
        variant="naked"
        title="Don't Just Take Our Word for It"
        description="See why hundreds of Orange County homeowners trust us with their plumbing. Read our 5-star reviews."
      >
        <template #body>
          <div class="flex justify-center items-center">
            <SocialMedia size="xl" />
          </div>
        </template>
      </UPageCTA>
      <TestimonialMarquee />
      <div class="flex justify-center mt-14">
        <UPageCTA
          title="Let's Get Your Plumbing Done Right"
          variant="subtle"
          :links="links"
          class="w-250 mb-30"
          description="If you're dealing with a plumbing issue or need an estimate, send me a message. I'll get back to you as soon as possible."
        />
      </div>
    </UPageSection>
  </div>
</template>

<script lang="ts" setup>
import services from '@/assets/services.json'
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
