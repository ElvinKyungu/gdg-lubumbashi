<template>
  <BaseHeader/>
  <main class="mt-20 mb-10">
    <h1 class="text-7xl font-bold text-center my-10">DevFest Lubumbashi 2024</h1>
    <div class="grid space-x-20 grid-cols-12">
      <div class="col-span-2">
      </div>
      <div class="col-span-4">
        <img class="shad object-contain shadow-2xl rounded-lg" src="@/assets/images/eventHeader.gif" alt="">
      </div>
      <div class="col-span-4">
        <p class="col-span-9 rounded-lg">
          DevFests are local tech conferences hosted by Google Developer Groups (GDG) around the world. Each DevFest event is crafted by its local organizers to fit the needs and interests of its local developer community. Whether it be through hands-on learning experiences, technical talks delivered in local languages by experts, or by simply meeting fellow local developers, DevFest attendees learn how to build together and innovate on Google’s developer tools.
        </p>
        <ul class="flex space-x-4 mt-5">
          <li class="flex gap-2">
            <IconsCalendar/>
            <span>
              November 9th, 2024
            </span>
          </li>
          <li class="flex gap-2">
            <IconsMap/>
            <span class="border-b">
              Concordia University Conference Center
            </span>
          </li>
        </ul>
        <button class="py-3 px-5 mt-5 bg-black text-white rounded-full">Get Tickets</button>
      </div>
      <div class="col-span-2">
      </div>
    </div>
  </main>
  <BaseFooter/>
</template>