<template>
  <div
    class="relative bg-cover bg-center bg-no-repeat"
    :style="{ backgroundImage: `url(${imagePath})` }"
  >
    <div class="absolute inset-0 bg-black/60" />
    <UPageHero
      :title="title"
      :description="description"
      :links="links"
      class="relative z-10"
    />
  </div>
</template>

<script lang="ts" setup>
interface HeroLink {
  label: string
  to: string
  icon?: string
  trailingIcon?: string
  size?: 'xs' | 'sm' | 'md' | 'lg' | 'xl'
  color?: 'error' | 'neutral' | 'primary' | 'secondary' | 'success' | 'info' | 'warning'
  variant?: 'solid' | 'outline' | 'soft' | 'subtle' | 'ghost' | 'link'
}

defineProps<{
  title: string
  description?: string
  links?: HeroLink[]
  imagePath: string
}>()
</script>

<style>

</style>
