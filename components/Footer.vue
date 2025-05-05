<template>
  <footer class="bg-gray-900 text-white py-10 px-6">
    <div class="max-w-6xl mx-auto grid md:grid-cols-2 gap-6 items-center">
      <!-- Brand -->
      <div>
        <h3 class="text-2xl font-semibold">Rayuma Living</h3>
        <p class="text-gray-400 mt-2 max-w-md">
          A trusted name in real estate. Discover high-quality homes and properties across Indonesia with expert guidance every step of the way.
        </p>
      </div>

      <!-- Navigation / Contact -->
      <div class="flex flex-col md:items-end gap-2 text-sm text-gray-400">
        <span>Email: contact@rayumaliving.com</span>
        <span>Phone: +62 812 3456 7890</span>
        <span>WhatsApp: +62 812 3456 7890</span>
        <span class="mt-4">© {{ new Date().getFullYear() }} Rayuma Living. All rights reserved.</span>
      </div>
    </div>
  </footer>
</template>
