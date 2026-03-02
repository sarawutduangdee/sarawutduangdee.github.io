<script setup lang="ts">
import SkillCard from '../ui/SkillCard.vue'

export interface Skill {
  label: string
  badge: string
  badgeColor?: string
}

defineProps<{
  title?: string
  skills: Skill[]
}>()
</script>

<template>
  <section id="skills" class="py-20">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
      <h2 class="text-3xl font-bold text-slate-900 mb-12">{{ title ?? 'My Tech Stack' }}</h2>
      <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-6">
        <SkillCard
          v-for="skill in skills"
          :key="skill.label"
          :label="skill.label"
          :badge="skill.badge"
          :badge-color="skill.badgeColor"
        />
      </div>
    </div>
  </section>
</template>
