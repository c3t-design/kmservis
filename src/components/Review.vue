<script setup lang="ts">
import ReviewCard from './ReviewCard.vue'
</script>

<template>
  <div class="bg-blue-primary text-center py-4">
    <h1 class="text-orange-primary text-3xl pt-4 font-bold">
      Pročitajte komentare naših klijenata
    </h1>
    <div class="grid lg:grid-cols-5 grid-cols-1 gap-8 px-8 pt-8 text-left text-blue-dark">
      <ReviewCard
        name="Anita A. P."
        comment="Covjek se javio brzo i isporucio uslugu kvalitetno i u dogovorenom roku. Posao je napravljen odlicno, jako smo zadovoljni. "
      />
      <ReviewCard
        name="Azmir A."
        comment="Prezadovoljan sam izvedbom montaže — sve odrađeno kvalitetno i čvrsto. Dali su odlične savjete oko podešavanja i održavanja, stvarno su objasnili šta treba raditi. Držali su se rokova, stigli i završili kad su rekli. Profesionalan i korektan pristup, preporuka. "
      />
      <ReviewCard
        name="Tina B."
        comment="Meni su dali odlične savjete, uvijek se jave na poziv i drže dogovorene rokove. Bili su ljubazni, detaljni u objašnjenjima i zaista pouzdani — točno ono što sam tražila. Topla preporuka! "
      />
      <ReviewCard
        name="Zdravko D."
        comment=" Vrlo profesionalan odnos pri kupnji novog klima uređaja — sve je bilo korektno, jasno i bez suvišnog kompliciranja, stvarno zadovoljan. "
      />
      <ReviewCard
        name="Ingo R."
        comment="ekipa je stvarno došla točno kako smo se dogovorili i sve rastavila i očistila do zadnjeg vijka. Objansili su mi hrpu sitnica kako da sama održavam klimu pa ne moram zvati svakih par mjeseci. Sve ide uredno, bez žurbe ali i bez razvlačenja, vidi se ozbiljan pristup. Ukratko, mogu mirno spavati kad znam da je klima u pouzdnim rukama. "
      />
    </div>
    <h3 class="pt-8 text-orange-primary text-xl">Pročitajte i ostale recenzije:</h3>
    <div class="flex items-center justify-center py-8">
      <div id="svc_embd_947" class="sticky bottom-12">
        <a
          href="https://www.trebam.hr/providers/km-servis-obrt-za-instalacije-montazu-odrzavanje-i-kucne-popravke-vl-ivan-dorcic"
        >
          <img
            alt="Klima uređaji, Montaža namještaja, Vodoinstalateri"
            src="https://www.trebam.hr/img/rating/km-servis-obrt-za-instalacije-montazu-odrzavanje-i-kucne-popravke-vl-ivan-dorcic_rating.png?embed_rating_image"
            class="h-auto w-auto justify-self-center m-auto"
        /></a>
      </div>
    </div>
    <div class="text-sm text-white-400 pb-2">
      <p>U kategorijama Klima uređaji, Vodoinstalateri i Kućni majstori</p>
    </div>
  </div>
</template>
