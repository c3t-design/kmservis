<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<template>
  <div class="h-[35px] bg-orange-primary"></div>
  <header class="bg-blue-primary grid grid-cols-2">
    <div class="p-4">
      <RouterLink to="/">
        <img src="/src/assets/logo.svg" alt="Vue logo" class="logo" />
      </RouterLink>
    </div>
    <nav class="text-xl text-white justify-self-end flex gap-8 self-center pr-8">
      <RouterLink to="/" class="p-4">O nama</RouterLink>
      <RouterLink to="/services" class="p-4">Galerija</RouterLink>
      <div class="rounded-lg bg-orange-primary p-4">
        <RouterLink to="/contact">Kontakt</RouterLink>
      </div>
    </nav>
  </header>
</template>
