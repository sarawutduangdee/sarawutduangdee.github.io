<script setup lang="ts">
import ProjectCard from '../ui/ProjectCard.vue'

export interface Project {
  title: string
  description: string
  image: string
  imageAlt?: string
  tags: { label: string; color?: string }[]
  linkUrl?: string
}

defineProps<{
  title?: string
  projects: Project[]
}>()
</script>

<template>
  <section id="projects" class="py-20">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <h2 class="text-3xl font-bold text-slate-900 mb-12 text-center">{{ title ?? 'Recent Projects' }}</h2>
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <ProjectCard
          v-for="project in projects"
          :key="project.title"
          :title="project.title"
          :description="project.description"
          :img="project.image"
          :image-alt="project.imageAlt"
          :tags="project.tags"
          :link-url="project.linkUrl"
        />
      </div>
    </div>
  </section>
</template>
