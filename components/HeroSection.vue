<template>
  <section class="relative bg-cover bg-center min-h-[80vh] flex items-center justify-center text-white"
           style="background-image: url('/images/hero.jpg');">
    <div class="absolute inset-0 bg-black/50 z-0" />
    <div class="relative z-10 text-center max-w-2xl px-4">
      <h1 class="text-4xl md:text-5xl font-semibold tracking-tight">
        Find Your Perfect Home with <span class="text-emerald-300">Rayuma Living</span>
      </h1>
      <p class="mt-4 text-lg md:text-xl text-gray-200">
        Kami bantu wujudkan rumah impian Anda dengan pilihan properti terbaik dan layanan terpercaya.
      </p>
      <NuxtLink to="#properties" class="mt-6 inline-block bg-emerald-500 hover:bg-emerald-600 text-white py-3 px-6 rounded-xl font-medium transition">
        Lihat Properti Sekarang
      </NuxtLink>
    </div>
  </section>
</template>
