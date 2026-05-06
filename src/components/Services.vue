<script setup lang="ts">
import ACBrands from './ACBrands.vue'

// Add component logic here
</script>

<template>
  <div id="services-section" class="hidden lg:block">
    <div
      class="bg-orange-primary grid gap-36 md:grid-cols-2 items-center justify-center px-18 py-16"
    >
      <div class="justify-self-end text-white max-w-lg">
        <h1 class="text-3xl font-bold px-8 pb-2">SERVIS KLIMA UREĐAJA</h1>
        <p class="px-8 text-lg">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
          ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation
          ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur
          sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id
          est laborum.
        </p>
      </div>
      <img
        src="/src/assets/ACSTOCK.jpg"
        alt="Service Image"
        class="w-auto h-auto max-h-[300px] mt-4 shadow-md justify-self-start"
      />
    </div>
    <ACBrands class="md:col-span-2" />
    <div class="text-blue-dark grid gap-36 md:grid-cols-2 items-center justify-center px-36 py-16">
      <img
        src="/src/assets/montaža.webp"
        alt="Service Image"
        class="w-auto h-auto max-h-[300px] mt-4 shadow-md justify-self-end"
      />
      <div class="justify-self-start max-w-lg">
        <h1 class="text-3xl font-bold px-8 pb-2">MONTAŽA NAMJEŠTAJA</h1>
        <p class="px-8 text-lg">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
          ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation
          ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur
          sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id
          est laborum.
        </p>
      </div>
    </div>
    <div
      class="text-blue-dark grid lg:gap-36 md:grid-cols-2 items-center justify-center px-36 py-16"
    >
      <div class="justify-self-end max-w-lg">
        <h1 class="text-3xl font-bold px-8 pb-2">VODOINSTALATERSKI RADOVI</h1>
        <p class="px-8 text-lg">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
          ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation
          ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur
          sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id
          est laborum.
        </p>
      </div>
      <img
        src="/src/assets/vodoinstalater.webp"
        alt="Service Image"
        class="w-auto max-h-[300px] h-auto mt-4 shadow-md justify-self-start"
      />
    </div>
  </div>
</template>
