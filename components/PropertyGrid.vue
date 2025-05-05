<template>
  <section id="properties" class="py-20 px-6 bg-gray-100">
    <div class="max-w-6xl mx-auto text-center mb-12">
      <h2 class="text-3xl md:text-4xl font-bold text-gray-800">Featured Properties</h2>
      <p class="mt-2 text-gray-600">
        A curated selection of homes designed for comfort, style, and modern living.
      </p>
    </div>

    <div class="grid gap-8 sm:grid-cols-2 lg:grid-cols-3">
      <div
        v-for="(property, index) in properties"
        :key="index"
        class="bg-white rounded-xl shadow hover:shadow-lg transition overflow-hidden"
      >
        <img :src="property.image" :alt="property.title" class="w-full h-52 object-cover" />

        <div class="p-5 text-left">
          <h3 class="text-xl font-semibold text-gray-800">{{ property.title }}</h3>
          <p class="text-gray-500 mt-1">{{ property.location }}</p>
          <p class="text-emerald-600 font-bold mt-3">{{ property.price }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const properties = [
  {
    title: 'Modern Family Home',
    location: 'Greenhill District, Bali',
    price: '$420,000',
    image: '/images/property-1.jpg'
  },
  {
    title: 'Luxury Beachfront Villa',
    location: 'Nusa Dua, Bali',
    price: '$980,000',
    image: '/images/property-2.jpg'
  },
  {
    title: 'Urban Smart Condo',
    location: 'Jakarta Selatan',
    price: '$310,000',
    image: '/images/property-3.jpg'
  }
]
</script>
