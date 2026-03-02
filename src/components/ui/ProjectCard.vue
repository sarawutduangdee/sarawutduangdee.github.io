<script setup lang="ts">
defineProps<{
  title: string
  description: string
  img: string
  imageAlt?: string
  tags: { label: string; color?: string }[]
  linkUrl?: string
}>()
</script>

<template>
  <div
    class="bg-white rounded-2xl overflow-hidden shadow-sm border border-slate-100 hover:shadow-xl transition-all group"
  >
    <div class="aspect-video bg-slate-200 overflow-hidden">
      <img
        :src="img"
        :alt="(imageAlt ?? title)?.replace(/(image|photo|picture|รูปภาพ)/i, '').trim()"
        class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500"
      />
    </div>
    <div class="p-6">
      <h3 class="text-xl font-bold text-slate-900 mb-2">{{ title }}</h3>
      <p class="text-slate-600 text-sm mb-4">{{ description }}</p>
      <div class="flex flex-wrap gap-2 mb-6">
        <span
          v-for="tag in tags"
          :key="tag.label"
          :class="['px-2 py-1 text-xs font-semibold rounded', tag.color || 'bg-slate-50 text-slate-600']"
        >
          {{ tag.label }}
        </span>
      </div>
      <a
        :href="linkUrl ?? '#'"
        class="inline-flex items-center text-indigo-600 font-bold hover:underline"
      >
        View Project
        <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path d="M14 5l7 7m0 0l-7 7m7-7H3" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" />
        </svg>
      </a>
    </div>
  </div>
</template>
