<script setup lang="ts">
// Footer component logic can be added here if needed
</script>

<template>
  <footer class="bg-blue-primary text-white py-8 w-full">
    <div class="w-full grid grid-cols-1 lg:grid-cols-2 gap-8 px-4">
      <!-- Left Column -->
      <div class="justify-self-center text-center lg:text-left">
        <div>
          <h3 class="text-lg font-bold mb-4">KM SERVIS</h3>
          <p class="text-sm">Obrt za instalacije, montažu, održavanje i kućne popravke</p>
        </div>
        <br />
        <div>
          <p>+385912345678</p>
          <p>email@firma.com</p>
        </div>
      </div>
      <!-- Right Column -->
      <div class="justify-self-center hidden lg:block">
        <br />
        <ul class="text-sm space-y-2">
          <li><router-link to="/" class="hover:underline">O nama</router-link></li>
          <li><router-link to="#services-section" class="hover:underline">Usluge</router-link></li>
          <li><router-link to="/contact" class="hover:underline">Kontakt</router-link></li>
          <li><router-link to="/gallery" class="hover:underline">Galerija</router-link></li>
        </ul>
      </div>
    </div>
  </footer>
</template>
