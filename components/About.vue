<template>
    <section id="home" class="pt-36 bg-no-repeat bg-center bg-fixed bg-cover ">
        <div class="container">
            <div class="flex flex-wrap">
                <div class="w-full h-16 self-center px-10 lg:w-1/2">
                    <h1 class="text-base font-semibold md:text-xl text-[#facc15] font-Fredoka ">Hi Semua 👋, saya <span
                            class="type mt-1 block text-4xl font-bold text-dark lg:text-5xl text-white font-fredoka">Dimas
                            Adhyaksa</span></h1>
                    <h2 class="mb-5 text-lg font-medium text-secondary lg:text-2xl text-slate-300">Web Developer & <span
                            class="text-dar text-[#facc15]">Creator</span></h2>
                    <NuxtLink to="/project/"
                        class="rounded-full bg-[#fdba74] py-3 px-8 text-base font-semibold text-slate-900  transition duration-300 ease-in-out hover:opacity-80 hover:shadow-lg">
                        My Project
                        <!-- <svg role="img" width="20" height="20" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><title>GitHub</title><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg> -->
                    </NuxtLink>
                </div>
                <div class="w-full self-end px-4 lg:w-1/2">
                    <div class="relative mt-10 lg:right-0 lg:mt-9">
                        <img src="~/assets/image/cat-coding.png" alt="Sandhika Galih"
                            class="relative z-10 mx-auto max-w-full" />
                        <span class="absolute bottom-0 left-1/2 -translate-x-1/2 md:scale-125">
                            <!-- <svg width="400" height="400" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                                <path fill="#14b8a6"
                                    d="M47.4,-51C59.2,-35.6,65.1,-17.8,63.4,-1.7C61.7,14.5,52.6,28.9,40.8,36.6C28.9,44.2,14.5,45,-2,47C-18.4,49,-36.8,52.1,-45.4,44.5C-53.9,36.8,-52.5,18.4,-51.2,1.3C-49.9,-15.8,-48.7,-31.7,-40.2,-47.1C-31.7,-62.4,-15.8,-77.3,1,-78.3C17.8,-79.2,35.6,-66.3,47.4,-51Z"
                                    transform="translate(100 100) scale(1.1)" />
                            </svg> -->
                        </span>
                    </div>
                </div>
            </div>
        </div>
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
            <path fill="#27272a" fill-opacity="1"
                d="M0,32L12.6,69.3C25.3,107,51,181,76,197.3C101.1,213,126,171,152,154.7C176.8,139,202,149,227,160C252.6,171,278,181,303,176C328.4,171,354,149,379,133.3C404.2,117,429,107,455,138.7C480,171,505,245,531,272C555.8,299,581,277,606,266.7C631.6,256,657,256,682,224C707.4,192,733,128,758,133.3C783.2,139,808,213,834,250.7C858.9,288,884,288,909,266.7C934.7,245,960,203,985,165.3C1010.5,128,1036,96,1061,101.3C1086.3,107,1112,149,1137,149.3C1162.1,149,1187,107,1213,122.7C1237.9,139,1263,213,1288,224C1313.7,235,1339,181,1364,144C1389.5,107,1415,85,1427,74.7L1440,64L1440,320L1427.4,320C1414.7,320,1389,320,1364,320C1338.9,320,1314,320,1288,320C1263.2,320,1238,320,1213,320C1187.4,320,1162,320,1137,320C1111.6,320,1086,320,1061,320C1035.8,320,1011,320,985,320C960,320,935,320,909,320C884.2,320,859,320,834,320C808.4,320,783,320,758,320C732.6,320,707,320,682,320C656.8,320,632,320,606,320C581.1,320,556,320,531,320C505.3,320,480,320,455,320C429.5,320,404,320,379,320C353.7,320,328,320,303,320C277.9,320,253,320,227,320C202.1,320,177,320,152,320C126.3,320,101,320,76,320C50.5,320,25,320,13,320L0,320Z">
            </path>
        </svg>
    </section>

    <!-- about s -->
    <section id="about" class="pt-10 dark:bg-dark bg-[#27272a]">
        <div class="container">
            <div class="flex flex-wrap">
                <div class="w-full self-center px-10 lg:w-1/2">
                    <h4 class="mb-3 text-lg font-bold text-slate-300">Tentang Saya</h4>
                    <h2 class="mb-0 max-w-md text-3xl font-bold text-dark text-[#facc15] lg:text-4xl font-Fredoka">
                        Dimas.
                    </h2>
                    <p class="max-w-xl text-base font-medium lg:text-lg text-white">Lorem ipsum dolor sit amet
                        consectetur adipisicing elit. Id temporibus maiores sequi vitae saepe iusto deleniti sukas suka
                        ksukasdkfhlhih kh !</p>
                    <p class="text-[#facc15] pt-2">Yuk bisa berteman!!</p>
                    <div class="medsos flex item-center pt-2">
                        <!-- istagram -->
                        <a href="https://instagram.com/sandhikagalih" target="_blank"
                            class="mr-3 flex h-9 w-9 items-center justify-center rounded-full border border-slate-300 text-slate-300 hover:border-[#facc15] hover:bg-[#facc15] hover:text-white">
                            <svg role="img" width="20" class="fill-current" viewBox="0 0 24 24"
                                xmlns="http://www.w3.org/2000/svg">
                                <title>Instagram</title>
                                <path
                                    d="M12 0C8.74 0 8.333.015 7.053.072 5.775.132 4.905.333 4.14.63c-.789.306-1.459.717-2.126 1.384S.935 3.35.63 4.14C.333 4.905.131 5.775.072 7.053.012 8.333 0 8.74 0 12s.015 3.667.072 4.947c.06 1.277.261 2.148.558 2.913.306.788.717 1.459 1.384 2.126.667.666 1.336 1.079 2.126 1.384.766.296 1.636.499 2.913.558C8.333 23.988 8.74 24 12 24s3.667-.015 4.947-.072c1.277-.06 2.148-.262 2.913-.558.788-.306 1.459-.718 2.126-1.384.666-.667 1.079-1.335 1.384-2.126.296-.765.499-1.636.558-2.913.06-1.28.072-1.687.072-4.947s-.015-3.667-.072-4.947c-.06-1.277-.262-2.149-.558-2.913-.306-.789-.718-1.459-1.384-2.126C21.319 1.347 20.651.935 19.86.63c-.765-.297-1.636-.499-2.913-.558C15.667.012 15.26 0 12 0zm0 2.16c3.203 0 3.585.016 4.85.071 1.17.055 1.805.249 2.227.415.562.217.96.477 1.382.896.419.42.679.819.896 1.381.164.422.36 1.057.413 2.227.057 1.266.07 1.646.07 4.85s-.015 3.585-.074 4.85c-.061 1.17-.256 1.805-.421 2.227-.224.562-.479.96-.899 1.382-.419.419-.824.679-1.38.896-.42.164-1.065.36-2.235.413-1.274.057-1.649.07-4.859.07-3.211 0-3.586-.015-4.859-.074-1.171-.061-1.816-.256-2.236-.421-.569-.224-.96-.479-1.379-.899-.421-.419-.69-.824-.9-1.38-.165-.42-.359-1.065-.42-2.235-.045-1.26-.061-1.649-.061-4.844 0-3.196.016-3.586.061-4.861.061-1.17.255-1.814.42-2.234.21-.57.479-.96.9-1.381.419-.419.81-.689 1.379-.898.42-.166 1.051-.361 2.221-.421 1.275-.045 1.65-.06 4.859-.06l.045.03zm0 3.678c-3.405 0-6.162 2.76-6.162 6.162 0 3.405 2.76 6.162 6.162 6.162 3.405 0 6.162-2.76 6.162-6.162 0-3.405-2.76-6.162-6.162-6.162zM12 16c-2.21 0-4-1.79-4-4s1.79-4 4-4 4 1.79 4 4-1.79 4-4 4zm7.846-10.405c0 .795-.646 1.44-1.44 1.44-.795 0-1.44-.646-1.44-1.44 0-.794.646-1.439 1.44-1.439.793-.001 1.44.645 1.44 1.439z" />
                            </svg>
                        </a>
                        <!-- X -->
                        <a href="https://twitter.com/sandhikagalih" target="_blank"
                            class="mr-3 flex h-9 w-9 items-center justify-center rounded-full border border-slate-300 text-slate-300 hover:border-[#facc15] hover:bg-[#facc15] hover:text-white">
                            <svg role="img" width="20" class="fill-current" viewBox="0 0 24 24"
                                xmlns="http://www.w3.org/2000/svg">
                                <title>Twitter</title>
                                <path
                                    d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z" />
                            </svg>
                        </a>
                        <!-- LinkedIn -->
                        <a href="https://linkedin.com/in/sandhikagalih" target="_blank"
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
                <div class="w-full self-end px-4 lg:w-1/2">
                    <div class="relative mt-10 lg:right-0 lg:mt-9 ">
                        <img src="~/assets/image/cat-coding.png" alt="Sandhika Galih"
                            class="relative z-10 mx-auto max-w-full hover:rotate-180" />
                        <span class="absolute bottom-0 left-1/2 -translate-x-1/2 md:scale-125">
                            <!-- <svg width="400" height="400" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                                    <path fill="#14b8a6"
                                        d="M47.4,-51C59.2,-35.6,65.1,-17.8,63.4,-1.7C61.7,14.5,52.6,28.9,40.8,36.6C28.9,44.2,14.5,45,-2,47C-18.4,49,-36.8,52.1,-45.4,44.5C-53.9,36.8,-52.5,18.4,-51.2,1.3C-49.9,-15.8,-48.7,-31.7,-40.2,-47.1C-31.7,-62.4,-15.8,-77.3,1,-78.3C17.8,-79.2,35.6,-66.3,47.4,-51Z"
                                        transform="translate(100 100) scale(1.1)" />
                                </svg> -->
                        </span>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>

</script>

<style scoped>
#home {
    background-image: url(@/assets/image/bg1.jpg);


}

</style>
