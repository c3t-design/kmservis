<script setup lang="ts">
import { onMounted, ref } from 'vue'

const slides = ref<Array<HTMLElement | null>>([])
const slideContainer = ref<HTMLElement | null>(null)
const currentIndex = ref(0)

const images = [
  {
    src: './src/assets/ACSTOCK.jpg',
    alt: 'AC stock image',
    text: 'Servis i montaža klima uređaja',
  },
  { src: './src/assets/montaža.webp', alt: 'Montaža', text: 'Montaža namještaja i kućni popravci' },
  {
    src: './src/assets/vodoinstalater.webp',
    alt: 'Review stock',
    text: 'Vodoinstalaterski radovi',
  },
]

const scrollToSlide = (index: number) => {
  const slide = slides.value[index]
  const container = slideContainer.value
  if (!slide || !container) return
  currentIndex.value = index
  const slideWidth = slide.offsetWidth
  const slideLeft = slide.offsetLeft
  container.scrollLeft = slideLeft - (container.offsetWidth - slideWidth) / 2
}

const prevSlide = () => {
  console.log('Previous button clicked')
  if (currentIndex.value <= 0) return
  scrollToSlide(currentIndex.value - 1)
}

const nextSlide = () => {
  console.log('Next button clicked')
  if (currentIndex.value >= images.length - 1) return
  scrollToSlide(currentIndex.value + 1)
}

onMounted(() => {
  scrollToSlide(currentIndex.value)
})
</script>

<template>
  <section class="py-12">
    <div class="flex items-center justify-center">
      <div class="relative overflow-hidden lg:max-w-[75%]">
        <div
          ref="slideContainer"
          class="flex snap-x snap-mandatory overflow-x-hidden overflow-y-hidden scroll-smooth"
        >
          <div
            v-for="(image, index) in images"
            :key="image.src"
            :ref="
              (el) => {
                slides[index] = el as HTMLElement | null
              }
            "
            class="slide snap-center shrink-0 w-full px-3 flex justify-center"
          >
            <div class="relative">
              <img
                :src="image.src"
                :alt="image.alt"
                class="h-[28rem] max-w-full object-contain block"
              />
              <div class="absolute inset-0 flex items-center justify-center rounded-[1.75rem]">
                <div class="bg-white/70 w-full px-6 py-4 text-center">
                  <p class="text-blue-dark font-semibold text-lg">{{ image.text }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <button
          type="button"
          @click="prevSlide"
          class="absolute left-3 top-1/2 -translate-y-1/2 rounded-full bg-none text-orange-primary p-3 text-5xl font-bold transition hover:bg-white"
          aria-label="Previous slide"
        >
          &#x2039;
        </button>

        <button
          type="button"
          @click="nextSlide"
          class="absolute right-3 top-1/2 -translate-y-1/2 rounded-full bg-none text-orange-primary p-3 text-5xl font-bold transition hover:bg-white"
          aria-label="Next slide"
        >
          &#x203A;
        </button>
      </div>
    </div>
  </section>
</template>
