<template>
  <footer class="bg-gray-900 text-white py-12 px-6">
    <div class="max-w-6xl mx-auto grid md:grid-cols-2 gap-10 items-start">
      <!-- Brand & Description -->
      <div>
        <h3 class="text-2xl font-serif font-semibold">Rayuma Living</h3>
        <p class="text-gray-400 mt-3 max-w-md font-sans leading-relaxed">
          A trusted name in real estate. Discover elegant homes across Indonesia with tailored guidance and unmatched service.
        </p>
      </div>

      <!-- Contact Info -->
      <div class="flex flex-col md:items-end text-sm text-gray-400 font-sans gap-1">
        <span>Email: contact@rayumaliving.com</span>
        <span>Phone: +62 812 3456 7890</span>
        <span>WhatsApp: +62 812 3456 7890</span>
        <span class="mt-4">© {{ new Date().getFullYear() }} Rayuma Living. All rights reserved.</span>
      </div>
    </div>
  </footer>
</template>
