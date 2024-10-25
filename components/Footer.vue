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
    const templateID = 'template_7xi2cav'
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
                    I’m <span class="font-semibold text-[#facc15]">Dimas Adhayaksa</span>, a Full Stack Web Developer. I
                    code just for fun & love it.
                </p>
                <div class="medsos flex item-center pt-2">
                    <!-- istagram -->
                    <a href="https://instagram.com/dimasadhyaksa_" target="_blank"
                        class="mr-3 flex h-9 w-9 items-center justify-center rounded-full border border-slate-300 text-slate-300 hover:border-[#facc15] hover:bg-[#facc15] hover:text-white">
                        <svg role="img" width="20" class="fill-current" viewBox="0 0 24 24"
                            xmlns="http://www.w3.org/2000/svg">
                            <title>Instagram</title>
                            <path
                                d="M12 0C8.74 0 8.333.015 7.053.072 5.775.132 4.905.333 4.14.63c-.789.306-1.459.717-2.126 1.384S.935 3.35.63 4.14C.333 4.905.131 5.775.072 7.053.012 8.333 0 8.74 0 12s.015 3.667.072 4.947c.06 1.277.261 2.148.558 2.913.306.788.717 1.459 1.384 2.126.667.666 1.336 1.079 2.126 1.384.766.296 1.636.499 2.913.558C8.333 23.988 8.74 24 12 24s3.667-.015 4.947-.072c1.277-.06 2.148-.262 2.913-.558.788-.306 1.459-.718 2.126-1.384.666-.667 1.079-1.335 1.384-2.126.296-.765.499-1.636.558-2.913.06-1.28.072-1.687.072-4.947s-.015-3.667-.072-4.947c-.06-1.277-.262-2.149-.558-2.913-.306-.789-.718-1.459-1.384-2.126C21.319 1.347 20.651.935 19.86.63c-.765-.297-1.636-.499-2.913-.558C15.667.012 15.26 0 12 0zm0 2.16c3.203 0 3.585.016 4.85.071 1.17.055 1.805.249 2.227.415.562.217.96.477 1.382.896.419.42.679.819.896 1.381.164.422.36 1.057.413 2.227.057 1.266.07 1.646.07 4.85s-.015 3.585-.074 4.85c-.061 1.17-.256 1.805-.421 2.227-.224.562-.479.96-.899 1.382-.419.419-.824.679-1.38.896-.42.164-1.065.36-2.235.413-1.274.057-1.649.07-4.859.07-3.211 0-3.586-.015-4.859-.074-1.171-.061-1.816-.256-2.236-.421-.569-.224-.96-.479-1.379-.899-.421-.419-.69-.824-.9-1.38-.165-.42-.359-1.065-.42-2.235-.045-1.26-.061-1.649-.061-4.844 0-3.196.016-3.586.061-4.861.061-1.17.255-1.814.42-2.234.21-.57.479-.96.9-1.381.419-.419.81-.689 1.379-.898.42-.166 1.051-.361 2.221-.421 1.275-.045 1.65-.06 4.859-.06l.045.03zm0 3.678c-3.405 0-6.162 2.76-6.162 6.162 0 3.405 2.76 6.162 6.162 6.162 3.405 0 6.162-2.76 6.162-6.162 0-3.405-2.76-6.162-6.162-6.162zM12 16c-2.21 0-4-1.79-4-4s1.79-4 4-4 4 1.79 4 4-1.79 4-4 4zm7.846-10.405c0 .795-.646 1.44-1.44 1.44-.795 0-1.44-.646-1.44-1.44 0-.794.646-1.439 1.44-1.439.793-.001 1.44.645 1.44 1.439z" />
                        </svg>
                    </a>
                    <!-- X -->
                    <a href="https://twitter.com/" target="_blank"
                        class="mr-3 flex h-9 w-9 items-center justify-center rounded-full border border-slate-300 text-slate-300 hover:border-[#facc15] hover:bg-[#facc15] hover:text-white">
                        <svg role="img" width="20" class="fill-current" viewBox="0 0 24 24"
                            xmlns="http://www.w3.org/2000/svg">
                            <title>Twitter</title>
                            <path
                                d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z" />
                        </svg>
                    </a>
                    <!-- LinkedIn -->
                    <a href="https://linkedin.com/in/dimas-adhyaksa-2105832b3/" target="_blank"
                        class="mr-3 flex h-9 w-9 items-center justify-center rounded-full border border-slate-300 text-slate-300 hover:border-[#facc15] hover:bg-[#facc15] hover:text-white">
                        <svg role="img" width="20" class="fill-current" viewBox="0 0 24 24"
                            xmlns="http://www.w3.org/2000/svg">
                            <title>LinkedIn</title>
                            <path
                                d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z" />
                        </svg>
                    </a>
                </div>
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
                                <NuxtLink to="/">About Me</NuxtLink>
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