<script setup lang="ts">
defineProps<{
  label: string
  badgeColor?: string
}>()
</script>

<template>
  <span
    :class="[
      'inline-flex items-center justify-center px-4 py-2.5 rounded-xl text-sm font-semibold shadow-sm border border-transparent',
      badgeColor || 'bg-indigo-50 text-indigo-600'
    ]"
  >
    {{ label }}
  </span>
</template>
