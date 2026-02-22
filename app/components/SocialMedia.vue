<template>
  <UButton
    to="https://www.facebook.com/profile.php?id=61587620072002"
    target="_blank"
    icon="i-simple-icons-facebook"
    aria-label="Facebook"
    color="neutral"
    variant="ghost"
    :size="size"
  />
  <UButton
    to="https://www.facebook.com/profile.php?id=61587620072002"
    target="_blank"
    icon="i-simple-icons-instagram"
    aria-label="Instagram"
    color="neutral"
    variant="ghost"
    :size="size"
  />
  <UButton
    to="https://www.yelp.com/biz/effective-plumbing-services-mission-viejo-2"
    target="_blank"
    icon="i-simple-icons-yelp"
    aria-label="Yelp"
    color="neutral"
    variant="ghost"
    :size="size"
  />
  <UButton
    to="https://www.thumbtack.com/ca/mission-viejo/affordable-plumbing-services/effective-plumbing-services-corporation/service/443470001512144916"
    target="_blank"
    icon="i-simple-icons-thumbtack"
    aria-label="Thumbtack"
    color="neutral"
    variant="ghost"
    :size="size"
  />
</template>

<script lang="ts" setup>
const { size = 'md' } = defineProps<{
  size?: 'xs' | 'sm' | 'md' | 'lg' | 'xl'
}>()
</script>

<style>

</style>
