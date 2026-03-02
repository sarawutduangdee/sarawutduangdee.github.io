<script setup lang="ts">
defineProps<{
  copyright?: string
  links?: { label: string; href: string }[]
}>()
</script>

<template>
  <footer class="py-12 bg-slate-50 border-t border-slate-200">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col md:flex-row justify-between items-center">
      <div class="text-slate-500 text-sm mb-4 md:mb-0">
        {{ copyright ?? '© 2023 Developer Portfolio. All rights reserved. Built with Vue 3 & Tailwind.' }}
      </div>
      <div class="flex space-x-6 text-sm">
        <a
          v-for="link in (links ?? [
            { label: 'Twitter', href: '#' },
            { label: 'GitHub', href: '#' },
            { label: 'LinkedIn', href: '#' }
          ])"
          :key="link.label"
          :href="link.href"
          class="text-slate-400 hover:text-indigo-600 transition-colors"
        >
          {{ link.label }}
        </a>
      </div>
    </div>
  </footer>
</template>
