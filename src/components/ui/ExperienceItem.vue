<script setup lang="ts">
defineProps<{
  role: string
  period: string
  company: string
  description: string
}>()
</script>

<template>
  <div class="relative pl-8">
    <span class="timeline-dot" />
    <div class="flex flex-col md:flex-row md:justify-between mb-2">
      <h3 class="text-xl font-bold text-slate-900">{{ role }}</h3>
      <span class="text-indigo-600 font-semibold">{{ period }}</span>
    </div>
    <h4 class="text-slate-700 font-medium mb-3">{{ company }}</h4>
    <p class="text-slate-600">{{ description }}</p>
  </div>
</template>
