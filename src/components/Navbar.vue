<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<template>
  <div class="sticky top-0 z-5">
    <div class="h-[10px] lg:h-[35px] bg-orange-primary"></div>
    <header class="bg-blue-primary grid lg:grid-cols-2 grid-cols-1">
      <div class="p-4">
        <RouterLink to="/">
          <img src="/src/assets/logo.svg" alt="Vue logo" class="logo" />
        </RouterLink>
      </div>
      <nav
        class="text-xl text-white hidden lg:justify-self-end lg:flex lg:gap-8 lg:self-center pr-8"
      >
        <RouterLink to="/" class="p-4">O nama</RouterLink>
        <RouterLink to="/gallery" class="p-4">Galerija</RouterLink>
        <div class="rounded-lg bg-orange-primary p-4">
          <RouterLink to="/contact">Kontakt</RouterLink>
        </div>
      </nav>
    </header>
  </div>
</template>
