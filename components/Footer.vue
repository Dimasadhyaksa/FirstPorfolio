<script setup>
import { ref } from 'vue'
import emailjs from '@emailjs/browser'

// State variables
const formData = ref({
    email: '',
})

const isSuccess = ref(false)
const isError = ref(false)
const isLoading = ref(false)

// Function to handle email sending
const sendEmail = async () => {
    // Start loading
    isLoading.value = true

    // Service, template, and user IDs
    const serviceID = 'service_oorl9ya'
    const templateID = 'template_24uvosc'
    const userID = "JVfGOCzLmFECTcyo0"

    try {
        // Sending email via EmailJS
        await emailjs.send(serviceID, templateID, {
            email: formData.value.email, // Use email from formData
            message: 'Your custom message here'
        }, userID)

        // Show success state
        isSuccess.value = true
        isError.value = false

        // Reset form data
        formData.value = { email: '' }

        // Hide success message after 4 seconds
        setTimeout(() => {
            isSuccess.value = false
        }, 4000)

    } catch (error) {
        // Handle error state
        isError.value = true
        isSuccess.value = false

        // Hide error message after 4 seconds
        setTimeout(() => {
            isError.value = false
        }, 4000)
    } finally {
        // Stop loading
        isLoading.value = false
    }
}
</script>


<template>
    <footer class="pt-16 pb-8 border-t dark:border-gray-600 sm:mb-0">
        <div class="container mx-auto px-6 grid grid-cols-1 md:grid-cols-10 gap-10">
            <div class="col-span-1 md:col-span-4">
                <h5 class="text-slate-700 font-semibold">Who Am I?</h5>
                <p class="my-4 block sm:w-10/12 text-slate-500">
                    I’m <span class="font-semibold text-black">Dimas Adhayaksa</span>, a Full Stack Web Developer. I
                    code just for fun & love it.
                </p>
                <SocialMedia />
            </div>
            <div class="col-span-1 md:col-span-6">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
                    <div>
                        <h3 class="font-semibold text-lg text-slate-700">Quick Links</h3>
                        <ul class="mt-4 text-slate-500">
                            <li>
                                <NuxtLink to="/">Home</NuxtLink>
                            </li>
                            <li>
                                <NuxtLink to="/About/">About Me</NuxtLink>
                            </li>
                            <li>
                                <NuxtLink to="/project/">Project</NuxtLink>
                            </li>
                            <li>
                                <NuxtLink to="/contact/">Contact</NuxtLink>
                            </li>
                        </ul>
                    </div>
                    <div>
                        <h3 class="font-semibold text-lg text-slate-700">Connect</h3>
                        <p class="text-sm mt-4 text-slate-500">
                            If you need me for business, you can send your email.
                        </p>
                        <form @submit.prevent="sendEmail" id="email-form">
                            <input id="email"
                                class="mt-3 bg-slate-100 focus:border-[#facc15] focus:outline-none focus:ring-1 focus:ring-[#facc15]  rounded-sm w-full"
                                type="email" v-model="formData.email" placeholder="Enter your email" required />

                            <!-- Submit button with loading spinner -->
                            <button v-if="!isLoading" type="submit"
                                class="btn w-full rounded-md bg-[#fdba74] text-white mt-3 btn-send">
                                Send
                            </button>

                            <div v-else class="flex justify-center btn-loading mt-3">
                                <svg aria-hidden="true"
                                    class="w-8 h-8 text-gray-200 animate-spin dark:text-gray-600 fill-[#fdba74]"
                                    viewBox="0 0 100 101" fill="none" xmlns="http://www.w3.org/2000/svg">
                                    <path
                                        d="M100 50.5908C100 78.2051 77.6142 100.591 50 100.591C22.3858 100.591 0 78.2051 0 50.5908C0 22.9766 22.3858 0.59082 50 0.59082C77.6142 0.59082 100 22.9766 100 50.5908ZM9.08144 50.5908C9.08144 73.1895 27.4013 91.5094 50 91.5094C72.5987 91.5094 90.9186 73.1895 90.9186 50.5908C90.9186 27.9921 72.5987 9.67226 50 9.67226C27.4013 9.67226 9.08144 27.9921 9.08144 50.5908Z"
                                        fill="currentColor" />
                                    <path
                                        d="M93.9676 39.0409C96.393 38.4038 97.8624 35.9116 97.0079 33.5539C95.2932 28.8227 92.871 24.3692 89.8167 20.348C85.8452 15.1192 80.8826 10.7238 75.2124 7.41289C69.5422 4.10194 63.2754 1.94025 56.7698 1.05124C51.7666 0.367541 46.6976 0.446843 41.7345 1.27873C39.2613 1.69328 37.813 4.19778 38.4501 6.62326C39.0873 9.04874 41.5694 10.4717 44.0505 10.1071C47.8511 9.54855 51.7191 9.52689 55.5402 10.0491C60.8642 10.7766 65.9928 12.5457 70.6331 15.2552C75.2735 17.9648 79.3347 21.5619 82.5849 25.841C84.9175 28.9121 86.7997 32.2913 88.1811 35.8758C89.083 38.2158 91.5421 39.6781 93.9676 39.0409Z"
                                        fill="currentFill" />
                                </svg>
                                <span class="sr-only">Loading...</span>
                            </div>

                            <!-- Success message -->
                            <p v-if="isSuccess" class="text-green-600 mt-3">Email sent successfully!</p>

                            <!-- Error message -->
                            <p v-if="isError" class="text-red-600 mt-3">Failed to send email. Please try again.</p>
                        </form>
                    </div>
                </div>
            </div>
        </div>
        <div class="container mx-auto px-6">
            <hr class="mt-10 mb-6 dark:border-gray-600" />
            <div class="text-slate-700">
                &copy; 2024. Who cares? It's <a href="https://github.com/dimasadhyaksa" target="_blank" rel="nofollow"
                    class="underline text-blue-500">open source</a>
            </div>
        </div>
    </footer>
</template>