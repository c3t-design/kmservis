<script setup lang="ts">
import { ref } from 'vue'

const name = ref('')
const email = ref('')
const message = ref('')
const isSubmitting = ref(false)
const successMessage = ref('')
const errorMessage = ref('')

const handleSubmit = async (event: Event) => {
  event.preventDefault()
  successMessage.value = ''
  errorMessage.value = ''

  if (!name.value.trim() || !email.value.trim() || !message.value.trim()) {
    errorMessage.value = 'Please fill in all fields.'
    return
  }

  const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/
  if (!emailPattern.test(email.value)) {
    errorMessage.value = 'Please enter a valid email address.'
    return
  }

  isSubmitting.value = true

  try {
    await new Promise<void>((resolve) => setTimeout(() => resolve(), 500))
    successMessage.value = 'Your message has been sent successfully. We will reply shortly.'
    name.value = ''
    email.value = ''
    message.value = ''
  } catch (error) {
    errorMessage.value = 'Unable to send your message. Please try again later.'
  } finally {
    isSubmitting.value = false
  }
}
</script>

<template>
  <div class="contact px-4 py-16 lg:py-36 md:px-8" id="contact">
    <div class="text-blue-dark text-center flex items-center justify-center">
      <!--md:grid-cols-2-->
      <div>
        <h1 class="text-5xl font-semibold mb-4 text-orange-primary pb-4">KONTAKT</h1>
        <div class="text-lg py-4">
          <p>Kontaktirajte nas na telefonski broj:</p>
          <p class="font-bold text-xl">+385981234567</p>
        </div>
        <div class="text-lg py-4">
          <p>Ili nam pošaljite email na:</p>
          <p class="font-bold text-xl">info@firma.hr</p>
        </div>
      </div>

      <!-- <div>
        <form
          @submit="handleSubmit"
          class="space-y-4 bg-white/90 dark:bg-slate-900/90 p-6 rounded-2xl shadow-sm border border-slate-200 dark:border-slate-700"
        >
          <div
            v-if="successMessage"
            class="rounded-xl bg-emerald-50 border border-emerald-200 px-4 py-3 text-sm text-emerald-800 dark:bg-emerald-900/80 dark:text-emerald-200"
          >
            {{ successMessage }}
          </div>

          <div
            v-if="errorMessage"
            class="rounded-xl bg-rose-50 border border-rose-200 px-4 py-3 text-sm text-rose-800 dark:bg-rose-900/80 dark:text-rose-200"
          >
            {{ errorMessage }}
          </div>

          <div>
            <label class="block text-sm font-medium mb-1" for="name">Name</label>
            <input
              id="name"
              v-model="name"
              type="text"
              placeholder="Your name"
              class="w-full rounded-xl border border-slate-300 px-4 py-3 text-sm focus:border-blue-500 focus:outline-none focus:ring-2 focus:ring-blue-200"
            />
          </div>

          <div>
            <label class="block text-sm font-medium mb-1" for="email">Email</label>
            <input
              id="email"
              v-model="email"
              type="email"
              placeholder="you@example.com"
              class="w-full rounded-xl border border-slate-300 px-4 py-3 text-sm focus:border-blue-500 focus:outline-none focus:ring-2 focus:ring-blue-200"
            />
          </div>

          <div>
            <label class="block text-sm font-medium mb-1" for="message">Message</label>
            <textarea
              id="message"
              v-model="message"
              rows="5"
              placeholder="Tell us how we can help"
              class="w-full rounded-xl border border-slate-300 px-4 py-3 text-sm focus:border-blue-500 focus:outline-none focus:ring-2 focus:ring-blue-200"
            ></textarea>
          </div>

          <button
            type="submit"
            :disabled="isSubmitting"
            class="inline-flex w-full items-center justify-center rounded-xl bg-blue-600 px-5 py-3 text-sm font-semibold text-white hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-300 disabled:cursor-not-allowed disabled:bg-blue-400"
          >
            {{ isSubmitting ? 'Sending...' : 'Send Message' }}
          </button>
        </form>
      </div> -->
    </div>
  </div>
</template>
