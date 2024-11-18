<template>
  <footer class="bg-slate-100 py-10 px-5 md:px-20">
    <div class="grid grid-cols-1 md:grid-cols-12 gap-10 items-center">
      <div class="col-span-1 md:col-span-4 space-y-4 text-center md:text-left">
        <nuxt-link to="/" class="flex items-center justify-center md:justify-start space-x-2">
          <img src="@/assets/images/logo.png" alt="Logo" class="w-20">
          <span class="text-lg font-medium">GDG Lubumbashi</span>
        </nuxt-link>
        <p class="text-sm text-gray-700">
          GDG Lubumbashi is a local tech community focused on learning, sharing, and innovating with Google technologies and beyond.
        </p>
      </div>
      <div class="col-span-1 md:col-span-4 flex justify-center">
        <ul class="flex md:flex-row items-center space-x-4 md:space-x-6 md:space-y-0">
          <li>
            <nuxt-link to="/" class="hover:text-green-400 transition">Home</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/about" class="hover:text-green-400 transition">About</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/services" class="hover:text-green-400 transition">Team</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/contact" class="hover:text-green-400 transition">Contact</nuxt-link>
          </li>
        </ul>
      </div>
      <div class="col-span-1 md:col-span-4 flex justify-center">
        <div class="flex space-x-4">
          <nuxt-link to="https://twitter.com" target="_blank" class="hover:text-green-400">
            <IconsX class="text-2xl" />
          </nuxt-link>
          <nuxt-link to="https://linkedin.com" target="_blank" class="hover:text-green-400">
            <IconsLinkedin class="text-2xl" />
          </nuxt-link>
          <nuxt-link to="https://youtube.com" target="_blank" class="hover:text-green-400">
            <IconsYoutube class="text-2xl" />
          </nuxt-link>
        </div>
      </div>
    </div>

    <div class="mt-10 border-t border-slate-400 pt-4 text-center text-sm text-gray-700">
      &copy; 2024 GDG Lubumbashi. All rights reserved.
    </div>
  </footer>
</template>
