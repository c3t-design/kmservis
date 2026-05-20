<script setup lang="ts">
import { onMounted, ref, watch } from 'vue'

const slides = ref<Array<HTMLElement | null>>([])
const slideContainer = ref<HTMLElement | null>(null)
const imageIndex = ref(0)
const disabledNext = ref(false)
const disabledPrevious = ref(true)

const images = [
  {
    src: './src/assets/ACSTOCK.jpg',
    alt: 'AC stock image',
    text: 'Servis i montaža klima uređaja',
  },
  { src: './src/assets/montaža.webp', alt: 'Montaža', text: 'Kućni popravci i montaža namještaja' },
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
  imageIndex.value = index
  const slideWidth = slide.offsetWidth
  const slideLeft = slide.offsetLeft
  container.scrollLeft = slideLeft - (container.offsetWidth - slideWidth) / 2
}

const prevSlide = () => {
  if (imageIndex.value <= 0) {
    console.log(imageIndex.value)
    return
  }
  scrollToSlide(imageIndex.value - 1)
}

const nextSlide = () => {
  if (imageIndex.value >= images.length - 1) {
    return
  }
  scrollToSlide(imageIndex.value + 1)
}

onMounted(() => {
  scrollToSlide(imageIndex.value)
})

watch(imageIndex, (newIndex) => {
  disabledPrevious.value = newIndex <= 0
  disabledNext.value = newIndex >= images.length - 1
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
          :disabled="disabledPrevious"
          class="absolute left-3 top-1/2 -translate-y-1/2 rounded-full bg-none text-orange-primary/25 p-2 pb-3 sm:p-3 sm:pb-6 text-5xl sm:text-[100px] font-bold transition"
          :class="{ 'hover:bg-blue-primary text-orange-primary!': !disabledPrevious }"
          aria-label="Previous slide"
        >
          &#x2039;
        </button>

        <button
          type="button"
          @click="nextSlide"
          :disabled="disabledNext"
          class="absolute right-3 top-1/2 -translate-y-1/2 rounded-full bg-none text-orange-primary/25 p-2 pb-3 sm:p-3 sm:pb-6 text-5xl sm:text-[100px] font-bold transition"
          :class="{ 'hover:bg-blue-primary text-orange-primary!': !disabledNext }"
          aria-label="Next slide"
        >
          &#x203A;
        </button>
      </div>
    </div>
  </section>
</template>
