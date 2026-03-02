<script setup lang="ts">
</script>

<template>
  <form class="space-y-6" action="#" method="POST">
    <div>
      <label for="full-name" class="block text-sm font-semibold text-slate-700 mb-1">Full Name</label>
      <input
        id="full-name"
        name="full-name"
        type="text"
        placeholder="John Doe"
        class="w-full rounded-xl border border-slate-200 focus:ring-indigo-500 focus:border-indigo-500 text-slate-900 px-4 py-2"
      />
    </div>
    <div>
      <label for="email" class="block text-sm font-semibold text-slate-700 mb-1">Email Address</label>
      <input
        id="email"
        name="email"
        type="email"
        placeholder="john@example.com"
        class="w-full rounded-xl border border-slate-200 focus:ring-indigo-500 focus:border-indigo-500 text-slate-900 px-4 py-2"
      />
    </div>
    <div>
      <label for="message" class="block text-sm font-semibold text-slate-700 mb-1">Message</label>
      <textarea
        id="message"
        name="message"
        rows="4"
        placeholder="Tell me about your project..."
        class="w-full rounded-xl border border-slate-200 focus:ring-indigo-500 focus:border-indigo-500 text-slate-900 px-4 py-2"
      />
    </div>
    <button
      type="submit"
      class="w-full py-4 bg-indigo-600 text-white font-bold rounded-xl hover:bg-indigo-700 transition-colors shadow-lg shadow-indigo-200"
    >
      Send Message
    </button>
  </form>
</template>
