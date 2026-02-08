<template>
  <UAccordion :items="items" />
</template>

<script lang="ts" setup>
import type { AccordionItem } from '@nuxt/ui'

const items = ref<AccordionItem[]>([
  {
    label: 'How quickly can you respond to a plumbing emergency?',
    content: 'We offer same-day service for most plumbing emergencies in South Orange County. For urgent issues like burst pipes or major leaks, we prioritize getting to you as fast as possible.'
  },
  {
    label: 'Do you provide free estimates?',
    content: 'Yes! We provide free, no-obligation estimates for all plumbing services. We believe in transparent, upfront pricing with no hidden fees or surprises.'
  },
  {
    label: 'What areas do you serve?',
    content: 'We proudly serve South Orange County and surrounding areas, including Mission Viejo, Laguna Niguel, San Juan Capistrano, Dana Point, Ladera Ranch, and Rancho Santa Margarita.'
  },
  {
    label: 'Are you licensed and insured?',
    content: 'Absolutely. We are a fully licensed C-36 plumbing contractor in California with comprehensive liability insurance to protect you and your property.'
  },
  {
    label: 'What types of plumbing services do you offer?',
    content: 'We handle everything from routine drain cleaning and leak repairs to water heater installation, repiping, sewer line repair, and fixture replacements. No job is too big or too small.'
  },
  {
    label: 'What payment methods do you accept?',
    content: 'We accept all major credit cards, checks, and cash. Payment is due upon completion of the work unless other arrangements have been made in advance.'
  }
])
</script>
