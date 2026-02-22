<script setup lang="ts">
import services from '@/assets/services.json'
</script>

<template>
  <div>
    <!-- HERO  -->
    <ImageHero
      title="Your Local South Orange County Plumber"
      image-path="/hero.webp"
      description="Licensed C-36 contractor offering honest, high-quality plumbing services—from drain cleaning to water heater repairs."
      :links="[{
        label: 'Contact Us',
        to: '/contact',
        trailingIcon: 'i-lucide-arrow-right',
        size: 'xl'
      }, {
        label: 'Gallery',
        to: '/gallery',
        icon: 'i-lucide-gallery-vertical-end',
        size: 'xl',
        color: 'neutral',
        variant: 'subtle'
      }]"
    />

    <!-- PLUMBING SERVICES  -->
    <UPageSection
      id="features"
      title="Our Plumbing Services"
      description="From everyday fixes to urgent problems, we provide reliable plumbing solutions for homes across South Orange County."
      :features="services"
    />
    <!-- INTRODUCTION TO COMPANY  -->
    <UPageSection
      orientation="horizontal"
      reverse
      title="Expert Plumbing Services"
      headline="Servicing Orange County since 2001"
    >
      <template #description>
        <p>Offering dependable plumbing services across South Orange County. With decades of hands-on experience, we help homeowners avoid costly damage and unexpected repairs.</p>
      </template>

      <template #default>
        <NuxtImg
          src="serviceArea.png"
          alt="Mission Viejo Service Area"
          class="w-full max-w-md"
        />
      </template>

      <template #body>
        <div class="flex gap-6">
          <UButton
            to="/contact"
            label="Contact Us"
            trailing-icon="i-lucide-arrow-right"
            size="lg"
          />
          <div>
            <SocialMedia />
          </div>
        </div>
      </template>
    </UPageSection>

    <!-- insert component here  -->
    <UPageSection title="Why Homeowners Choose Effective Plumbing">
      <template #body>
        <div class="grid lg:grid-cols-2 gap-12 items-center">
          <!-- Left: Text Content -->
          <div>
            <div class="space-y-8">
              <div>
                <h3 class="text-xl font-semibold mb-2">
                  Family-Owned Since 2001
                </h3>
                <p class="text-gray-600 dark:text-gray-400">
                  For over 20 years, we've proudly served South Orange County homeowners with honest, dependable service. Our experience ensures every job is handled with care and attention to detail.
                </p>
              </div>

              <div>
                <h3 class="text-xl font-semibold mb-2">
                  Residential Expertise
                </h3>
                <p class="text-gray-600 dark:text-gray-400">
                  We specialize in residential plumbing—from single-family homes to condos and townhouses. Our team understands the unique needs of homeowners and delivers tailored solutions for every property.
                </p>
              </div>

              <div>
                <h3 class="text-xl font-semibold mb-2">
                  Local to Southern California
                </h3>
                <p class="text-gray-600 dark:text-gray-400">
                  We're based right here in Mission Viejo. Our team knows local building codes, common plumbing issues in the area, and what Southern California's climate can do to your pipes.
                </p>
              </div>
            </div>
          </div>

          <!-- Right: Image -->
          <div class="relative">
            <NuxtImg
              src="/bathtub.jpg"
              alt="Effective Plumbing Services team at work"
              class="rounded-lg shadow-lg w-full h-auto object-cover"
            />
          </div>
        </div>
      </template>
    </UPageSection>

    <UPageSection
      title="What people are saying about Effective Plumbing Services"
      description="Don't just take our word for it - hear from the families who we have worked with! Visit the contact page to read testimonials from families about their experiences with Effective Plumbing Services"
    >
      <UContainer>
        <TestimonialMarquee />
      </UContainer>
    </UPageSection>

    <ContactFormContainer />
  </div>
</template>
