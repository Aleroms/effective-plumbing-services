<template>
  <div>
    <!-- HERO  -->
    <div
      class="relative bg-cover bg-center bg-no-repeat"
      style="background-image: url('/hero.webp');"
    >
      <div class="absolute inset-0 bg-black/60" />
      <UPageHero
        title="Your Local South Orange County Plumber"
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
        class="relative z-10"
      />
    </div>

    <!-- PLUMBING SERVICES  -->
    <UPageSection
      id="features"
      title="Our Plumbing Services"
      description="From everyday fixes to urgent problems, we provide reliable plumbing solutions for homes across South Orange County."
      :features="[{
        icon: 'i-lucide-droplet-off',
        title: 'Residential Leak Detection',
        description: 'Using advanced detection equipment, we pinpoint hidden leaks in walls, foundations, and underground pipes—saving you from extensive water damage, mold growth, and inflated utility bills.'
      }, {
        icon: 'i-lucide-wrench',
        title: 'Drain Backups & Clogs',
        description: 'Stubborn clogs and sewer backups can disrupt your daily routine. We use professional-grade tools including hydro-jetting and drain cameras to clear blockages and identify underlying issues.'
      }, {
        icon: 'i-lucide-tool-case',
        title: 'Plumbing Service & Repair',
        description: 'Whether it\'s a dripping faucet, running toilet, or broken pipe, our experienced technicians diagnose and repair plumbing problems efficiently with upfront pricing and quality workmanship.'
      }, {
        icon: 'i-lucide-heater',
        title: 'Water Heater Services',
        description: 'No hot water? We service all brands and types—tank, tankless, gas, and electric. From routine maintenance to full replacements, we ensure reliable hot water year-round.'
      }, {
        icon: 'i-lucide-shower-head',
        title: 'Shower Valve Repair & Replacement',
        description: 'Inconsistent water temperature or weak pressure? We repair and replace faulty shower valves, cartridges, and mixing valves to restore a comfortable, safe showering experience.'
      }, {
        icon: 'i-lucide-bath',
        title: 'Tub & Fixture Repairs',
        description: 'Leaky faucets, outdated fixtures, or a cracked tub can affect both function and aesthetics. We repair, replace, and upgrade bathroom and kitchen fixtures to modern standards.'
      }]"
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
  </div>
</template>
