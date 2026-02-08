<template>
  <UPageSection
    title="Contact Us"
    description="Tell us about your project, and we'll get back to you within 24 hours"
  >
    <template #body>
      <USeparator />

      <div class="flex justify-evenly gap-12 mt-5">
        <ContactForm />
        <div class="space-y-8">
          <div>
            <div class="space-y-3">
              <p class="text-2xl font-bold text-primary">
                Effective Plumbing Services
              </p>
              <a
                href="tel:+19498134644"
                class="flex items-center gap-2 text-gray-600 dark:text-gray-400 hover:text-primary transition-colors"
              >
                <UIcon
                  name="i-lucide-phone"
                  class="size-5"
                />
                +1 (949) 813-4644
              </a>
              <a
                href="mailto:effectiveplumbingservices@gmail.com"
                class="flex items-center gap-2 text-gray-600 dark:text-gray-400 hover:text-primary transition-colors"
              >
                <UIcon
                  name="i-lucide-mail"
                  class="size-5"
                />
                effectiveplumbingservices@gmail.com
              </a>
            </div>
          </div>
          <div>
            <h3 class="text-lg font-semibold mb-3 flex items-center gap-2">
              <UIcon
                name="i-lucide-clock"
                class="size-5"
              />
              Hours
            </h3>
            <div class="space-y-1 text-gray-600 dark:text-gray-400">
              <p>Monday - Friday: 7:00 AM - 5:00 PM</p>
              <p>Saturday/Sunday: Closed</p>
              <p>Closed major holidays</p>
              <p class="text-sm text-primary mt-2">
                24/7 Emergency Service Available
              </p>
            </div>
          </div>
        </div>
      </div>
    </template>
  </UPageSection>
</template>

<script lang="ts" setup>

</script>

<style>

</style>
