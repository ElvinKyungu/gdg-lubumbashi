<script setup lang="ts">

</script>
<template>
  <section class="relative z-50 overflow-hidden">
    <div class="relative mx-auto w-full px-4 py-6 sm:px-6 lg:px-40 lg:py-20">
      <h1 class="text-3xl md:text-5xl xl:text-7xl font-bold text-center my-10">
        Last Year at DevFest Montreal
      </h1>
      <div class="flex justify-center my-10">
        <p class="max-w-xl text-center flex justify-center">Last year, we had 200+ attendees, 10+ speakers, 10+ sessions, and 1 amazing event.</p>
      </div>
      <div class="flex flex-col gap-10 md:flex-row">
        <div class="w-full md:w-1/2">
          <div class="flex flex-col gap-10 sm:flex-row">
            <div ref="firstImage" class="relative h-64 w-full overflow-hidden rounded-lg sm:w-1/2 lg:h-96">
              <img
                src="@/assets/images/chancy_cercle.jpg"
                alt="gallery"
                class="h-full w-full object-cover rounded-3xl"
              />
            </div>
            <div ref="secondImage" class="relative h-64 w-full overflow-hidden rounded-lg sm:w-1/2 lg:h-96">
              <img
                src="@/assets/images/empire_cercle.jpg"
                alt="gallery"
                class="h-full w-full object-cover rounded-3xl"
              />
            </div>
          </div>
          <div ref="thirtImage" class="relative mt-10 h-96 w-full overflow-hidden rounded-lg lg:h-[40rem]">
            <img
              src="@/assets/images/enjoy.jpg"
              alt="gallery"
              class="h-full w-full object-cover rounded-3xl"
            />
          </div>
        </div>
        <div class="w-full md:w-1/2">
          <div ref="fourthImage" class="relative h-96 w-full overflow-hidden rounded-lg lg:h-[40rem]">
            <img
              src="@/assets/images/SoftDay24-16.jpg"
              alt="gallery"
              class="h-full w-full object-cover rounded-3xl"
            />
          </div>
          <div  class="mt-10 flex flex-col gap-10 sm:flex-row">
            <div ref="fiveImage" class="relative h-64 w-full overflow-hidden rounded-lg sm:w-1/2 lg:h-96">
              <img
                src="@/assets/images/SoftDay24-46.jpg"
                alt="gallery"
                class="h-full w-full object-cover rounded-3xl"
              />
            </div>
            <div ref="sixImage" class="relative h-64 w-full overflow-hidden rounded-lg sm:w-1/2 lg:h-96">
              <img
                src="@/assets/images/panel.jpg"
                alt="gallery"
                class="h-full w-full object-cover rounded-3xl"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>