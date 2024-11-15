<script setup lang="ts">
import gsap from "gsap"

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
</script>


<template>
  <header class="flex justify-between py-3 px-10 items-center bg-slate-100">
    <nuxt-link to="/">
      <img class="w-40" src="@/assets/images/logo.png" alt="logo gdg">
    </nuxt-link>
    <nav>
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
    <nav class="flex ">
      <ul class="flex space-x-6">
        <li class="cursor-pointer">
          <nuxt-link to="">
            <IconsX />
          </nuxt-link>
        </li>
        <li>
          <nuxt-link to="">
            <IconsLinkedin/>
          </nuxt-link>
        </li>
        <li>
          <nuxt-link to="">
            <IconsYoutube/>
          </nuxt-link>
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

</style>