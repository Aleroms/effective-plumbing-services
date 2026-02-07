<script lang="ts" setup>
import type { UserProps } from '@nuxt/ui'

// name
// date

const testimonials: { user: UserProps, quote: string }[] = [
  {
    user: { name: 'Shin Karasuda', description: '4 months ago' },
    quote: 'I used George to replace a toilet, install 2 new faucets and a new sink. He did a great job. He is very meticulous, clean, professional and friendly. Just a great guy. I will always use George for my plumbing needs. Thanks George.'
  },
  {
    user: { name: 'Matt Wood', description: 'a month ago' },
    quote: 'George was very quick to get here to help, and offered a more than reasonable price. We are very happy with Effective Plumbing’s work. I would recommend him to anyone.'
  },
  {
    user: { name: 'Matthew Willey', description: '5 months ago' },
    quote: 'One call to George and he arrived within the hour. He was friendly and professional. He explained what was going on with my plumbing issue and recommended the least aggressive approach. He did not try to upsell.'
  },
  {
    user: { name: 'Ashley Walters', description: '2 years ago' },
    quote: 'George was our super hero! We had a leak from an upstairs bathroom that flooded our garage and he fixed everything. He came at the time he said he would.'
  },
  {
    user: { name: 'Melissa Clark', description: '9 months ago' },
    quote: 'We found George through the Nextdoor app after seeing multiple glowing recommendations, and we’re so glad we did. He did a fantastic job with our plumbing repairs and was very reasonably priced.'
  },
  {
    user: { name: 'Kei Kim', description: 'Edited 4 months ago' },
    quote: 'George is super friendly and attentive for all your plumbing needs. He makes sure that you understand everything he’s about to do. Great guy overall and very thorough.'
  },
  {
    user: { name: 'Gail N', description: 'a year ago' },
    quote: 'We are very pleased with our toilet removal and replacement. George was polite, prompt and had excellent workmanship. Highly recommend!'
  },
  {
    user: { name: 'pamela koshko', description: 'a year ago' },
    quote: 'George was responsive, arrived on time, and was friendly, knowledgeable and professional. He explained and showed me the problem and the cost was very reasonable.'
  },
  {
    user: { name: 'Meenakshi Natarajan', description: '2 years ago' },
    quote: 'George is very professional, kind and knowledgeable. He did a great job and cleaned up after the work. I will definitely recommend him.'
  },
  {
    user: { name: 'namrata patel', description: '4 months ago' },
    quote: 'It was great to work with George. He promptly responded to the call, provided same day service, was reasonable and very informative.'
  },
  {
    user: { name: 'Jerry Flores', description: '6 months ago' },
    quote: 'I have used George for several plumbing jobs and he always does a great job at a fair price.'
  },
  {
    user: { name: 'Angie San Mateo', description: '4 months ago' },
    quote: 'George responded promptly to our call. He was knowledgeable and professional. Will use him again.'
  },
  {
    user: { name: 'Michele Haddad', description: 'a year ago' },
    quote: 'George was amazing! He was at my house within 20 minutes, quick, professional, extremely personable, and reasonably priced.'
  },
  {
    user: { name: 'Jodi Harris', description: '2 years ago' },
    quote: 'I highly recommend George and Effective Plumbing Services. He is responsive, professional, and honest.'
  },
  {
    user: { name: 'Rachael', description: 'a year ago' },
    quote: 'Highly recommend George! Honest plumber. He came out fast, was very friendly, great prices, and truly cares about his clients.'
  },
  {
    user: { name: 'Sharad Venugopal', description: '2 years ago' },
    quote: 'Outstanding customer service and very professional. Excellent communication, on-time arrival, and high-quality work.'
  },
  {
    user: { name: 'Esther Fuller', description: '3 years ago' },
    quote: 'George was incredibly friendly, quick, efficient, and excellent at communicating. Very kind and respectful.'
  },
  {
    user: { name: 'Michael Cansler', description: '2 years ago' },
    quote: 'George is fantastic. He is an excellent communicator and delivers the same level of service he would for his own home.'
  },
  {
    user: { name: 'Eric Smith', description: '2 years ago' },
    quote: 'Awesome customer service. Very honest. George shows you what’s wrong and recommends what needs to be done.'
  },
  {
    user: { name: 'Lou Jr', description: 'a year ago' },
    quote: 'George did great plumbing work, was on time, and I will definitely be calling him again.'
  }
]
</script>

<template>
  <div class="flex flex-col gap-4 w-full overflow-hidden">
    <UMarquee
      pause-on-hover
      :overlay="false"
      :ui="{ root: '[--duration:100s] [--gap:--spacing(4)]', content: 'w-auto py-1' }"
    >
      <UPageCard
        v-for="(testimonial, index) in testimonials"
        :key="index"
        variant="subtle"
        :description="testimonial.quote"

        class="w-64 shrink-0"
        :ui="{
          description: 'before:content-[open-quote] after:content-[close-quote] line-clamp-4'
        }"
      >
        <template #footer>
          <UUser v-bind="testimonial.user" />
        </template>
      </UPageCard>
    </UMarquee>
    <UMarquee
      pause-on-hover
      :overlay="false"
      reverse
      :ui="{ root: '[--duration:100s] [--gap:--spacing(4)]', content: 'w-auto py-1' }"
    >
      <UPageCard
        v-for="(testimonial, index) in testimonials"
        :key="index"
        variant="subtle"
        :description="testimonial.quote"
        class="w-64 shrink-0"
        :ui="{
          description: 'before:content-[open-quote] after:content-[close-quote] line-clamp-4'
        }"
      >
        <template #footer>
          <UUser v-bind="testimonial.user" />
        </template>
      </UPageCard>
    </UMarquee>
  </div>
</template>
