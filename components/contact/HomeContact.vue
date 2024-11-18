<template>
  <section class="max-w-screen-3xl py-16  md:px-12 lg:px-16 xl:px-32">
    <div>
      <h1 class="text-3xl md:text-5xl ml-7 xl:text-6xl font-bold my-10">
        Let’s talk about everything!
      </h1>
    </div>
    <div class=" px-8 grid gap-8 grid-cols-1 md:grid-cols-2 mx-auto text-gray-900 rounded-lg">
      <div class="flex flex-col justify-between">
        <div class="mt-8 text-center">
          <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d15630.411072517514!2d27.472471299999984!3d-11.651629355159836!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x19723eb370268065%3A0xf383e16ffa7b7c9e!2sCentre%20de%20Conf%C3%A9rence%20ARRUPE!5e0!3m2!1sfr!2scd!4v1731917526805!5m2!1sfr!2scd" 
            class="w-full" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade">
          </iframe>
        </div>
      </div>
      <div class="relative h-[450px] flex mt-7 items-center justify-center">
        <div class="relative w-full overflow-hidden h-full">
          <div v-for="(image, index) in images" :key="index" 
            class="absolute inset-0 flex justify-center items-center slide"
            :class="{ 'opacity-0': index !== currentSlide, 'opacity-100': index === currentSlide }"
            ref="slides">
            <img :src="image" alt="" class="w-full h-full object-cover rounded-lg" />
          </div>
          <div class="absolute w-full h-full bg-black/50 rounded-lg "></div>
        </div>
  
        <button 
          @click="prevSlide"
          class="absolute left-4 top-1/2 -translate-y-1/2 bg-black/50 text-white p-2 rounded-full hover:bg-black/70">
          Prev
        </button>
        <button 
          @click="nextSlide"
          class="absolute right-4 bg-black/50 text-white p-2 rounded-full hover:bg-black/70">
          Next
        </button>
      </div>
    </div>
  </section>
  
</template>

<script setup lang="ts">
import gsap from "gsap"
import image1 from '@/assets/images/enjoy.jpg'
import image2 from '@/assets/images/SoftDay24-16.jpg'
import image3 from '@/assets/images/empire_cercle.jpg'

const images = [image1, image2, image3]
const currentSlide = ref(0)
const slides = ref<HTMLElement[]>([])

const showSlide = (index: number) => {
  const current = slides.value[currentSlide.value]
  const next = slides.value[index]

  // Animation sortante pour l'actuelle
  gsap.to(current, {
    opacity: 0,
    x: -50,
    duration: 0.5,
  })

  // Animation entrante pour la suivante
  gsap.fromTo(
    next,
    { opacity: 0, x: 50 },
    { opacity: 1, x: 0, duration: 0.5 }
  )

  currentSlide.value = index
}

const prevSlide = () => {
  const nextIndex = (currentSlide.value - 1 + images.length) % images.length
  showSlide(nextIndex)
}

const nextSlide = () => {
  const nextIndex = (currentSlide.value + 1) % images.length
  showSlide(nextIndex)
}

onMounted(() => {
  slides.value = Array.from(document.querySelectorAll('.slide')) as HTMLElement[]

  // Affiche la première image au chargement
  gsap.set(slides.value[currentSlide.value], {
    opacity: 1,
    x: 0,
  })
})
</script>

<style scoped>
.slide {
  position: absolute;
  inset: 0;
  opacity: 0;
  transition: opacity 0.5s ease, transform 0.5s ease;
}
</style>
