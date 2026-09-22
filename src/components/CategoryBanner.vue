<template>
  <div
    class="category-banner q-mb-lg"
    :style="{ backgroundImage: `url(${image})`, backgroundSize: 'cover', backgroundPosition: 'center 40%' }"
  >
    <div class="banner-overlay"></div>
    <div class="banner-content">
      <div class="banner-title text-weight-bold font-title">{{ title }}</div>
      <div class="banner-desc q-mt-xs">{{ description }}</div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  image: { type: String, required: true },
  title: { type: String, required: true },
  description: { type: String, required: true }
})
</script>
