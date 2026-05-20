<script setup lang="ts">
import ACBrands from './ACBrands.vue'

// Add component logic here
</script>

<template>
  <div id="services-section">
    <div
      class="bg-orange-primary grid gap-8 sm:gap-36 md:grid-cols-2 items-center justify-center px-6 sm:px-18 py-16"
    >
      <div class="justify-self-end text-white max-w-lg">
        <h1 class="text-3xl font-bold px-8 pb-2">SERVIS KLIMA UREĐAJA</h1>
        <p class="px-8 text-lg">
          Servis klima uređaja obuhvaća redovito održavanje, čišćenje filtera, provjeru rashladnog
          sustava i popravke kako bi uređaj radio pouzdano i energetski učinkovito. Naša usluga
          uključuje dijagnostiku neispravnosti, nadopunu plina i zamjenu oštećenih dijelova za
          optimalan rad vaše klime.
        </p>
      </div>
      <img
        src="/src/assets/ACSTOCK.jpg"
        alt="Service Image"
        class="w-auto h-auto max-h-[300px] mt-4 shadow-md justify-self-center sm:justify-self-start"
      />
    </div>
    <ACBrands class="md:col-span-2" />
    <div
      class="text-blue-dark grid gap-8 sm:gap-36 md:grid-cols-2 items-center justify-center px-6 sm:px-18 py-16"
    >
      <img
        src="/src/assets/montaža.webp"
        alt="Service Image"
        class="w-auto h-auto max-h-[300px] mt-4 shadow-md justify-self-center sm:justify-self-end"
      />
      <div class="justify-self-start max-w-lg order-first sm:order-none">
        <h1 class="text-3xl font-bold px-8 pb-2">KUĆNI POPRAVCI I MONTAŽA NAMJEŠTAJA</h1>
        <p class="px-8 text-lg">
          Rješavamo sitne kvarove i preinake koje vaš dom čine ugodnijim i praktičnijim. Radimo
          kućne popravke, od popravaka vrata, ormara i polica do sastavljanja novog namještaja,
          osiguravajući da vaš prostor bude funkcionalan i estetski privlačan.
        </p>
      </div>
    </div>
    <div
      class="text-blue-dark grid gap-8 sm:gap-36 md:grid-cols-2 items-center justify-center px-6 sm:px-18 py-16"
    >
      <div class="justify-self-end max-w-lg">
        <h1 class="text-3xl font-bold px-8 pb-2">VODOINSTALATERSKI RADOVI</h1>
        <p class="px-8 text-lg">
          Izvodimo vodoinstalaterske radove koji obuhvaćaju popravke cijevi, ugradnju sanitarija i
          otklanjanje curenja. Naša usluga uključuje brzo rješavanje hitnih problema i održavanje
          instalacija kako bi vaša voda uvijek protjecala bez zastoja.
        </p>
      </div>
      <img
        src="/src/assets/vodoinstalater.webp"
        alt="Service Image"
        class="w-auto max-h-[300px] h-auto mt-4 shadow-md justify-self-center sm:justify-self-start"
      />
    </div>
  </div>
</template>
