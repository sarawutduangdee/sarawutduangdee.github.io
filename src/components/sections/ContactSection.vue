<script setup lang="ts">
import ContactForm from '../ui/ContactForm.vue'

defineProps<{
  title?: string
  description?: string
  email?: string
  phone?: string
  location?: string
}>()
</script>

<template>
  <section id="contact" class="py-20 bg-slate-900 text-white">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid lg:grid-cols-2 gap-16">
        <div>
          <h2 class="text-4xl font-bold mb-6">{{ title ?? "Let's work together." }}</h2>
          <p class="text-slate-400 text-lg mb-10 max-w-md">
            {{ description ?? "Have a project in mind? Looking for a new addition to your team? I'm always open to discussing new opportunities and interesting projects." }}
          </p>
          <div class="space-y-6">
            <a v-if="email" :href="`mailto:${email}`" class="flex items-center text-white hover:text-indigo-300 transition-colors no-underline">
              <div class="w-12 h-12 bg-indigo-600/20 text-indigo-400 rounded-full flex items-center justify-center mr-4 shrink-0">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" />
                </svg>
              </div>
              <span class="text-lg font-medium">{{ email }}</span>
            </a>
            <a v-if="phone" :href="`tel:${phone.replace(/\s/g, '')}`" class="flex items-center text-white hover:text-indigo-300 transition-colors no-underline">
              <div class="w-12 h-12 bg-indigo-600/20 text-indigo-400 rounded-full flex items-center justify-center mr-4 shrink-0">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" />
                </svg>
              </div>
              <span class="text-lg font-medium">{{ phone }}</span>
            </a>
            <div v-if="location" class="flex items-center">
              <div class="w-12 h-12 bg-indigo-600/20 text-indigo-400 rounded-full flex items-center justify-center mr-4">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" />
                  <path d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" />
                </svg>
              </div>
              <span class="text-lg font-medium">{{ location }}</span>
            </div>
          </div>
        </div>
        <div class="bg-white rounded-3xl p-8 shadow-2xl">
          <ContactForm />
        </div>
      </div>
    </div>
  </section>
</template>
