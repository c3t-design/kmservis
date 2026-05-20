<script setup lang="ts">
import Contact from '@/components/Contact.vue'
import Landing from '@/components/Landing.vue'
import MobileHomeMessage from '@/components/MobileHomeMessage.vue'
import Review from '@/components/Review.vue'
import Services from '@/components/Services.vue'
</script>

<template>
  <main>
    <Landing />
    <Services />
    <MobileHomeMessage class="hidden" />
    <Review />
    <Contact />
  </main>
</template>
