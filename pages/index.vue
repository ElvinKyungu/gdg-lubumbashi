<template>
  <BaseHeader/>
  <main class="mt-20 mb-10">
    <h1 class="text-3xl md:text-5xl xl:text-7xl font-bold text-center my-10">
      DevFest Lubumbashi 2024
    </h1>
    <div class="grid grid-cols-1 lg:grid-cols-12 gap-5 lg:space-x-20 items-center">
      <!-- Empty space on larger screens -->
      <div class="hidden lg:block lg:col-span-2"></div>
  
      <!-- Image Section -->
      <div class="col-span-1 lg:col-span-4 flex justify-center">
        <img
          class="shad object-contain shadow-2xl rounded-lg w-full max-w-xs md:max-w-lg lg:max-w-none"
          src="@/assets/images/eventHeader.gif"
          alt="Event Header"
        />
      </div>
  
      <!-- Content Section -->
      <div class="col-span-1 lg:col-span-4">
        <p class="text-center lg:text-left rounded-lg p-5">
          DevFests are local tech conferences hosted by Google Developer Groups (GDG) around the world. Each DevFest
          event is crafted by its local organizers to fit the needs and interests of its local developer community.
          Whether it be through hands-on learning experiences, technical talks delivered in local languages by experts,
          or by simply meeting fellow local developers, DevFest attendees learn how to build together and innovate on
          Google’s developer tools.
        </p>
        <ul class="flex flex-col md:flex-row gap-4 text-base mt-5 items-center justify-center lg:justify-start">
          <li class="flex items-center gap-2">
            <IconsCalendar />
            <span>November 9th, 2024</span>
          </li>
          <li class="flex items-center gap-2">
            <IconsMap />
            <span class="border-b">Concordia University Conference Center</span>
          </li>
        </ul>
        <div class="flex justify-center lg:justify-start">
          <button class="py-3 px-5 mt-5 bg-black text-white rounded-full">
            Get Tickets
          </button>
        </div>
      </div>
  
      <!-- Empty space on larger screens -->
      <div class="hidden lg:block lg:col-span-2"></div>
    </div>
  
    <!-- GridHomeGrid Section -->
    <GridHomeGrid />
    <SponsorHomeSponsors/>
    <ContactHomeContact/>
  </main>
  <BaseFooter/>
</template>