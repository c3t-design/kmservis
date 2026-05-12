<script setup lang="ts">
import { RouterView } from 'vue-router'
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <Navbar />
  <RouterView />
  <Footer />
  <!-- <div class="sticky bottom-12 right-12">
    <div id="svc_embd_947" class="absolute right-12 bottom-6">
      <a
        href="https://www.trebam.hr/providers/km-servis-obrt-za-instalacije-montazu-odrzavanje-i-kucne-popravke-vl-ivan-dorcic"
      >
        <img
          alt="Klima uređaji, Montaža namještaja, Vodoinstalateri"
          src="https://www.trebam.hr/img/rating/km-servis-obrt-za-instalacije-montazu-odrzavanje-i-kucne-popravke-vl-ivan-dorcic_rating.png?embed_rating_image"
          class="w-auto h-auto"
      /></a>
    </div>
  </div> -->
</template>
