<script setup lang="ts">
defineProps<{
  role: string
  period: string
  company: string
  description: string
  highlights?: string[]
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
    <ul v-if="highlights?.length" class="mt-3 space-y-1.5 text-slate-600 list-disc pl-5">
      <li v-for="(point, i) in highlights" :key="i">{{ point }}</li>
    </ul>
  </div>
</template>
