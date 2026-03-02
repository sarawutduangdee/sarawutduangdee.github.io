<script setup lang="ts">
import ExperienceItem from '../ui/ExperienceItem.vue'

export interface Experience {
  role: string
  period: string
  company: string
  description: string
}

defineProps<{
  title?: string
  items: Experience[]
}>()
</script>

<template>
  <section id="experience" class="py-20 bg-slate-100">
    <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
      <h2 class="text-3xl font-bold text-slate-900 mb-12 text-center">{{ title ?? 'Work History' }}</h2>
      <div class="space-y-12 border-l-2 border-indigo-200 ml-4 lg:ml-0 relative">
        <ExperienceItem
          v-for="(item, i) in items"
          :key="i"
          :role="item.role"
          :period="item.period"
          :company="item.company"
          :description="item.description"
        />
      </div>
    </div>
  </section>
</template>
