<script setup lang="ts">
defineProps<{
  label: string
  badge: string
  badgeColor?: string
}>()
</script>

<template>
  <div
    class="p-6 bg-white rounded-2xl shadow-sm border border-slate-100 flex flex-col items-center hover:shadow-md transition-shadow"
  >
    <div
      :class="['w-12 h-12 mb-3 rounded-lg flex items-center justify-center font-bold', badgeColor || 'bg-indigo-50 text-indigo-600']"
    >
      {{ badge }}
    </div>
    <span class="font-semibold text-slate-700">{{ label }}</span>
  </div>
</template>
