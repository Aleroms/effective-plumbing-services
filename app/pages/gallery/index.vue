<template>
  <UPageSection
    title="Project Gallery"
    description="From pipe repairs to water heater installations, see the quality craftsmanship we bring to every job."
  >
    <div class="p-5 md:p-10">
      <div
        class="columns-1 sm:columns-2 lg:columns-3 gap-5 lg:gap-8
        [&>img:not(:first-child)]:mt-5 lg:[&>img:not(:first-child)]:mt-8"
      >
        <!-- only display the modal for medium and up  -->
        <UModal
          v-for="image in galleryImages"
          :key="image.src"
          class="cursor-pointer hidden md:block"
        >
          <NuxtImg
            format="webp"
            class="rounded-sm shadow-sm"
            width="300"
            :src="image.src"
            placeholder
          />
          <template #content>
            <NuxtImg
              key="index"
              format="webp"
              :src="image.src"
            />
          </template>
        </UModal>

        <!-- displays for mobile  -->
        <div class=" md:hidden flex flex-col justify-center [&>img:not(:first-child)]:mt-8">
          <NuxtImg
            v-for="(image, index) in galleryImages"
            :key="index"
            format="webp"
            class="rounded-sm"
            :src="image.src"
            placeholder
          />
        </div>
      </div>
    </div>
  </UPageSection>
</template>

<script lang="ts" setup>
interface GalleryImage {
  src: string
  alt: string
  caption: string
}

const galleryImages = ref<GalleryImage[]>([
  {
    src: '/pipes/pipe2.jpg',
    alt: 'Pipe repair work',
    caption: 'Pipe Repair & Replacement'
  },
  {
    src: '/pipes/pipe.jpg',
    alt: 'Professional pipe installation',
    caption: 'Copper Pipe Installation'
  },
  {
    src: '/pipes/pipe4.jpg',
    alt: 'Plumbing system maintenance',
    caption: 'System Maintenance'
  },
  {
    src: '/pipes/pipe5.jpg',
    alt: 'New plumbing installation',
    caption: 'New Construction Plumbing'
  },
  {
    src: '/bathtub.jpg',
    alt: 'Bathtub installation',
    caption: 'Bathroom Fixtures'
  },
  {
    src: '/pipes/water-heater.jpg',
    alt: 'Water heater installation',
    caption: 'Water Heater Installation'
  },
  {
    src: '/gallery/IMG_0018.jpg',
    alt: 'Plumbing project',
    caption: 'Recent Project'
  },
  {
    src: '/gallery/IMG_0019.jpg',
    alt: 'Plumbing project',
    caption: 'Recent Project'
  },
  {
    src: '/gallery/IMG_0021.jpg',
    alt: 'Plumbing project',
    caption: 'Recent Project'
  },
  {
    src: '/gallery/IMG_0205.jpg',
    alt: 'Plumbing project',
    caption: 'Recent Project'
  },
  {
    src: '/gallery/IMG_0207.jpg',
    alt: 'Plumbing project',
    caption: 'Recent Project'
  },
  {
    src: '/gallery/IMG_0208.jpg',
    alt: 'Plumbing project',
    caption: 'Recent Project'
  },
  {
    src: '/gallery/IMG_0334.jpg',
    alt: 'Plumbing project',
    caption: 'Recent Project'
  },
  {
    src: '/gallery/IMG_0336.jpg',
    alt: 'Plumbing project',
    caption: 'Recent Project'
  },
  {
    src: '/gallery/IMG_0352.jpg',
    alt: 'Plumbing project',
    caption: 'Recent Project'
  }
])
</script>

<style>

</style>
