<script setup lang="ts">
defineProps<{
  title?: string
  subtitle?: string
  paragraphs?: string[]
}>()
</script>

<template>
  <section id="about" class="py-20 bg-white">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid lg:grid-cols-3 gap-12">
        <div class="lg:col-span-1">
          <h2 class="text-sm font-bold uppercase tracking-widest text-indigo-600 mb-2">About Me</h2>
          <h3 class="text-3xl font-bold text-slate-900">
            {{ subtitle ?? 'Passionate about clean code and performance.' }}
          </h3>
        </div>
        <div class="lg:col-span-2 text-slate-600 leading-relaxed text-lg">
          <template v-for="(p, i) in (paragraphs ?? [])" :key="i">
            <p :class="i < (paragraphs?.length ?? 1) - 1 ? 'mb-6' : ''">{{ p }}</p>
          </template>
        </div>
      </div>
    </div>
  </section>
</template>
