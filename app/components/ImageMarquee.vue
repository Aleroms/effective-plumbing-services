<template>
  <UMarquee pause-on-hover>
    <NuxtImg
      v-for="path in imagePath"
      :key="path"
      :src="path"
      width="300"
      height="200"
    />
  </UMarquee>
</template>

<script lang="ts" setup>
const imagePath = [
  '/pipes/pipe.jpg',
  '/pipes/pipe2.jpg',
  '/pipes/pipe4.jpg',
  '/pipes/pipe5.jpg',
  '/pipes/water-heater.jpg'
]
</script>

<style>

</style>
