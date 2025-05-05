<template>
  <section class="py-20 px-6 bg-white">
    <div class="max-w-5xl mx-auto text-center mb-12">
      <h2 class="text-3xl md:text-4xl font-bold text-gray-800">Why Choose Rayuma Living?</h2>
      <p class="mt-2 text-gray-600">
        We go beyond listings — we deliver experiences, trust, and homes that inspire.
      </p>
    </div>

    <div class="grid gap-10 md:grid-cols-3 max-w-6xl mx-auto">
      <div v-for="(item, index) in reasons" :key="index" class="text-center px-6">
        <div class="w-14 h-14 mx-auto mb-4 rounded-full bg-emerald-100 flex items-center justify-center">
          <component :is="item.icon" class="w-6 h-6 text-emerald-600" />
        </div>
        <h3 class="text-lg font-semibold text-gray-800">{{ item.title }}</h3>
        <p class="text-gray-600 mt-2">{{ item.description }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ShieldCheckIcon, UsersIcon, HomeIcon } from 'lucide-vue-next'

const reasons = [
  {
    title: 'Trusted Expertise',
    description: 'Over 10 years of real estate experience with deep local insight.',
    icon: ShieldCheckIcon
  },
  {
    title: 'Tailored Service',
    description: 'Personalized assistance to match you with the perfect property.',
    icon: UsersIcon
  },
  {
    title: 'Curated Listings',
    description: 'Only premium, verified properties make it into our portfolio.',
    icon: HomeIcon
  }
]
</script>
