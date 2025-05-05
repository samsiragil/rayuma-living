<template>
  <section
    class="relative bg-cover bg-center min-h-[90vh] flex items-center justify-center text-white"
    style="background-image: url('/images/hero.jpg');"
  >
    <div class="absolute inset-0 bg-black/60 z-0" />

    <div class="relative z-10 text-center max-w-2xl px-6">
      <h1 class="text-4xl md:text-5xl font-bold tracking-tight leading-tight">
        Find Your Perfect Home<br />
        with <span class="text-emerald-400">Rayuma Living</span>
      </h1>

      <p class="mt-4 text-lg md:text-xl text-gray-200">
        We help you discover high-quality, dream-worthy properties with trusted service and tailored advice.
      </p>

      <NuxtLink
        to="#properties"
        class="mt-6 inline-block bg-emerald-500 hover:bg-emerald-600 text-white py-3 px-6 rounded-xl font-semibold transition"
      >
        Explore Listings
      </NuxtLink>
    </div>
  </section>
</template>
