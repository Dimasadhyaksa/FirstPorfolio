<template>
  <section id="contact" class="pt-28 pb-32 bg-[#27272a]">
    <div class="container">
      <div class="w-full px-4">
        <div class="mx-auto mb-16 max-w-xl text-center">
          <h2 class="mb-4 text-3xl font-bold text-white sm:text-4xl lg:text-5xl">Kontak Saya Disini</h2>
          <p class="text-md font-medium text-slate-300 md:text-lg">Jika ingin berinteraksi dengan saya, apapun akan saya
            bahas.^^</p>
        </div>
      </div>

      <!-- Pesan notifikasi -->
      <p v-if="isSuccess" class="text-center text-green-500">Pesan terkirim</p>
      <p v-if="isError" class="text-center text-red-500">Pesan gagal terkirim</p>
      <p v-if="isLoading" class="text-center text-blue-500">Mengirim pesan...</p>

      <!-- Formulir kontak -->
      <form @submit.prevent="sendEmail">
        <div class="w-full lg:mx-auto lg:w-2/3">
          <!-- Nama -->
          <div class="mb-8 w-full px-4">
            <label for="name" class="text-base font-bold text-[#facc15]">Nama</label>
            <input v-model="formData.name" type="text" id="name"
              class="w-full rounded-md bg-white p-3 text-dark focus:border-[#facc15] focus:outline-none focus:ring-1 focus:ring-[#facc15]" />
            <p v-if="formErrors.name" class="text-red-500 text-sm">Nama wajib diisi</p>
          </div>

          <!-- Email -->
          <div class="mb-8 w-full px-4">
            <label for="email" class="text-base font-bold text-[#facc15]">Email</label>
            <input v-model="formData.email" type="email" id="email"
              class="w-full rounded-md bg-white p-3 text-dark focus:border-[#facc15] focus:outline-none focus:ring-1 focus:ring-[#facc15]" />
            <p v-if="formErrors.email" class="text-red-500 text-sm">Email wajib diisi</p>
          </div>

          <!-- Pesan -->
          <div class="mb-8 w-full px-4">
            <label for="message" class="text-base font-bold text-[#facc15]">Pesan</label>
            <textarea v-model="formData.message" id="message"
              class="h-32 w-full rounded-md bg-white p-3 text-dark focus:border-[#facc15] focus:outline-none focus:ring-1 focus:ring-[#facc15]"></textarea>
            <p v-if="formErrors.message" class="text-red-500 text-sm">Pesan wajib diisi</p>
          </div>

          <!-- Tombol Kirim -->
          <div class="w-full px-4">
            <button v-if="!isLoading"
              class="w-full rounded-full bg-[#fdba74] py-3 px-8 text-base font-semibold text-white transition duration-500 hover:opacity-80 hover:shadow-lg">
              Kirim
            </button>
            <!-- Tombol Loading -->
            <button v-else
              class="w-full rounded-full bg-gray-500 py-3 px-8 text-base font-semibold text-white transition duration-500 cursor-not-allowed">
              Loading...
            </button>
          </div>
        </div>
      </form>
    </div>
  </section>
</template>



<script setup>
import { ref } from 'vue'
import emailjs from '@emailjs/browser'

const formData = ref({
  name: '',
  email: '',
  message: '',
})

const isSuccess = ref(false)
const isError = ref(false)
const isLoading = ref(false)
const formErrors = ref({
  name: false,
  email: false,
  message: false,
})

const validateForm = () => {
  let isValid = true

  // Periksa apakah semua field telah diisi
  formErrors.value.name = !formData.value.name
  formErrors.value.email = !formData.value.email
  formErrors.value.message = !formData.value.message

  if (!formData.value.name || !formData.value.email || !formData.value.message) {
    isValid = false
  }

  return isValid
}

const sendEmail = async () => {
  // Validasi sebelum mengirim email
  if (!validateForm()) {
    return // Jika tidak valid, hentikan proses pengiriman
  }

  isLoading.value = true // Tampilkan loading saat mulai proses pengiriman

  const serviceID = 'service_oorl9ya'
  const templateID = 'template_ndchvtj'
  const userID = "JVfGOCzLmFECTcyo0"

  try {
    await emailjs.send(serviceID, templateID, {
      form_name: formData.value.name,
      email: formData.value.email,
      message: formData.value.message,
    }, userID)
    
    isSuccess.value = true
    isError.value = false
    formData.value = { name: '', email: '', message: '' } // Reset form setelah sukses
  } catch (error) {
    isError.value = true
    isSuccess.value = false
  } finally {
    isLoading.value = false // Hentikan loading setelah selesai
    setTimeout(() => {
      isSuccess.value = false
      isError.value = false
    }, 4000)
  }
}
</script>

