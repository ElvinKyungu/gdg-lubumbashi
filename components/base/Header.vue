<script setup lang="ts">
import gsap from "gsap"

const isMenuOpen = ref(false)

onMounted(() => {
  const links = document.querySelectorAll(".nav-link")

  links.forEach(link => {
    const border = document.createElement("div")
    border.className = "border-anim"
    link.appendChild(border)

    link.addEventListener("mouseenter", () => {
      gsap.to(border, {
        width: "100%",
        duration: 0.2,
        ease: "power2.out",
      })
    })

    link.addEventListener("mouseleave", () => {
      gsap.to(border, {
        width: "0%",
        duration: 0.2,
        ease: "power2.out",
      })
    })
  })
})

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
  gsap.to(".mobile-menu", {
    height: isMenuOpen.value ? "auto" : "0",
    opacity: isMenuOpen.value ? 1 : 0,
    duration: 0.5,
    ease: "power2.out",
  })
}
</script>

<template>
  <header class="flex justify-between py-3 px-6 items-center bg-slate-100">
    <nuxt-link to="/">
      <img class="w-32 md:w-40" src="@/assets/images/logo.png" alt="logo gdg" />
    </nuxt-link>
    <nav class="hidden md:block">
      <ul class="flex space-x-6">
        <li class="cursor-pointer nav-link hover:text-green-500 transition duration-700">
          <nuxt-link to="">Home</nuxt-link>
        </li>
        <li class="cursor-pointer nav-link hover:text-green-500 transition duration-700">
          <nuxt-link to="">About</nuxt-link>
        </li>
        <li class="cursor-pointer nav-link hover:text-green-500 transition duration-700">
          <nuxt-link to="">Team</nuxt-link>
        </li>
        <li class="cursor-pointer nav-link hover:text-green-500 transition duration-700">
          <nuxt-link to="">Contact</nuxt-link>
        </li>
      </ul>
    </nav>
    <nav class="flex space-x-4">
      <nuxt-link to="">
        <IconsX />
      </nuxt-link>
      <nuxt-link to="">
        <IconsLinkedin />
      </nuxt-link>
      <nuxt-link to="">
        <IconsYoutube />
      </nuxt-link>
      <button class="block md:hidden" @click="toggleMenu">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
        </svg>
      </button>
    </nav>
    <!-- Mobile Menu -->
    <nav
      class="absolute top-16 left-0 w-full bg-slate-100 overflow-hidden mobile-menu md:hidden"
      style="height: 0; opacity: 0;"
    >
      <ul class="flex flex-col space-y-4 p-4">
        <li class="cursor-pointer nav-link hover:text-green-500 transition duration-700">
          <nuxt-link to="">Home</nuxt-link>
        </li>
        <li class="cursor-pointer nav-link hover:text-green-500 transition duration-700">
          <nuxt-link to="">About</nuxt-link>
        </li>
        <li class="cursor-pointer nav-link hover:text-green-500 transition duration-700">
          <nuxt-link to="">Team</nuxt-link>
        </li>
        <li class="cursor-pointer nav-link hover:text-green-500 transition duration-700">
          <nuxt-link to="">Contact</nuxt-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style>
.nav-link {
  position: relative;
  display: inline-block;
}

.nav-link .border-anim {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 2px;
  width: 0%;
  background-color: rgb(28, 201, 143);
  transition: width 0.2s ease-in-out;
}

.mobile-menu {
  transition: height 0.5s ease-out, opacity 0.5s ease-out;
}
</style>
