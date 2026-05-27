<template>
  <main class="gallery-page px-4 py-16 lg:px-24 bg-slate-50 text-slate-900">
    <section class="max-w-7xl mx-auto">
      <div class="mb-12 text-center">
        <p class="text-sm uppercase tracking-[0.4em] text-orange-primary">Galerija</p>
        <h1 class="mt-4 text-4xl font-bold sm:text-5xl">Pogledajte naše radove</h1>
        <p class="mx-auto mt-4 max-w-2xl text-base leading-7 text-slate-600">
          Prvi pregled fotografija s izvedenim projektima i servisima. Ove slike služe kao početna
          verzija galerije koja će kasnije biti dopunjena pravim materijalima.
        </p>
      </div>

      <div class="columns-1 sm:columns-2 xl:columns-3 gap-6 space-y-6">
        <article class="break-inside-avoid rounded-3xl overflow-hidden bg-white shadow-lg">
          <img
            src="@/assets/ACSTOCK.jpg"
            alt="Servis klima uređaja"
            class="w-full h-auto object-cover"
          />
          <div class="p-5">
            <h2 class="text-xl font-semibold">Servis klima uređaja</h2>
            <p class="mt-2 text-sm text-slate-600">
              Održavanje i popravak sustava za optimalnu funkcionalnost.
            </p>
          </div>
        </article>

        <article class="break-inside-avoid rounded-3xl overflow-hidden bg-white shadow-lg">
          <img
            src="@/assets/montaža.webp"
            alt="Montaža namještaja"
            class="w-full h-auto object-cover"
          />
          <div class="p-5">
            <h2 class="text-xl font-semibold">Montaža namještaja</h2>
            <p class="mt-2 text-sm text-slate-600">
              Brza i sigurna montaža s pažnjom prema detaljima.
            </p>
          </div>
        </article>

        <article class="break-inside-avoid rounded-3xl overflow-hidden bg-white shadow-lg">
          <img
            src="@/assets/vodoinstalater.webp"
            alt="Vodoinstalaterski radovi"
            class="w-full h-auto object-cover"
          />
          <div class="p-5">
            <h2 class="text-xl font-semibold">Vodoinstalaterski radovi</h2>
            <p class="mt-2 text-sm text-slate-600">
              Popravci cijevi, ugradnja sanitarija i rješavanje curenja.
            </p>
          </div>
        </article>

        <article class="break-inside-avoid rounded-3xl overflow-hidden bg-white shadow-lg">
          <img
            src="@/assets/stockreview.webp"
            alt="Povratne informacije"
            class="w-full h-auto object-cover"
          />
          <div class="p-5">
            <h2 class="text-xl font-semibold">Recenzije i povratne informacije</h2>
            <p class="mt-2 text-sm text-slate-600">
              Prikaz zadovoljnih klijenata i njihovih iskustava.
            </p>
          </div>
        </article>

        <article class="break-inside-avoid rounded-3xl overflow-hidden bg-white shadow-lg">
          <img
            src="@/assets/pngwing.com.png"
            alt="Radovi u kući"
            class="w-full h-auto object-cover"
          />
          <div class="p-5">
            <h2 class="text-xl font-semibold">Kućni popravci</h2>
            <p class="mt-2 text-sm text-slate-600">Svestrani popravci i dorade za svaki dom.</p>
          </div>
        </article>

        <article class="break-inside-avoid rounded-3xl overflow-hidden bg-white shadow-lg">
          <img
            src="@/assets/Vector.svg"
            alt="Grafički prikaz"
            class="w-full h-auto object-cover bg-slate-100"
          />
          <div class="p-5">
            <h2 class="text-xl font-semibold">Vizualni prikaz prostora</h2>
            <p class="mt-2 text-sm text-slate-600">
              Inicijalni vizualizacije i konfiguracije prostora.
            </p>
          </div>
        </article>
      </div>
    </section>
  </main>
</template>
