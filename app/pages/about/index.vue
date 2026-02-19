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
          src="https://scontent-lax3-1.cdninstagram.com/v/t39.30808-6/559133853_122146447784757273_1354492621437949740_n.jpg?stp=dst-jpg_e35_tt6&_nc_cat=102&ig_cache_key=MzczNTQ2NzI3Nzg3Nzg5MjAzOA%3D%3D.3-ccb7-5&ccb=7-5&_nc_sid=58cdad&efg=eyJ2ZW5jb2RlX3RhZyI6InhwaWRzLjUxOXg1NzYuc2RyLkMzIn0%3D&_nc_ohc=7oC5ZleowKcQ7kNvwEOamqb&_nc_oc=Adn6uULcjdPNvIw6q_sjY6a0IfVCLv8HMT-YM9SOzKTJdjTkXevU8tMZ0cmuZAOjy50xrIhOdIXqfbVYrgPppu3d&_nc_ad=z-m&_nc_cid=0&_nc_zt=23&_nc_ht=scontent-lax3-1.cdninstagram.com&_nc_gid=jdo-Ljh3K6_mNbA6fUqwfw&oh=00_Aftj5RUE5k6R7dHrrqPGLWjm76uXP1gFNZ4lzjU9czN_NQ&oe=699C784F"
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
