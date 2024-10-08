<template>
    <div id="main">
        <Header />
        <About />
        <!-- project s -->
        <section id="project" class="bg-center bg-cover bg-no-repeat bg-fixed">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
                <path fill="#27272a" fill-opacity="1"
                    d="M0,128L16,138.7C32,149,64,171,96,176C128,181,160,171,192,160C224,149,256,139,288,138.7C320,139,352,149,384,154.7C416,160,448,160,480,144C512,128,544,96,576,101.3C608,107,640,149,672,192C704,235,736,277,768,250.7C800,224,832,128,864,122.7C896,117,928,203,960,202.7C992,203,1024,117,1056,74.7C1088,32,1120,32,1152,37.3C1184,43,1216,53,1248,85.3C1280,117,1312,171,1344,165.3C1376,160,1408,96,1424,64L1440,32L1440,0L1424,0C1408,0,1376,0,1344,0C1312,0,1280,0,1248,0C1216,0,1184,0,1152,0C1120,0,1088,0,1056,0C1024,0,992,0,960,0C928,0,896,0,864,0C832,0,800,0,768,0C736,0,704,0,672,0C640,0,608,0,576,0C544,0,512,0,480,0C448,0,416,0,384,0C352,0,320,0,288,0C256,0,224,0,192,0C160,0,128,0,96,0C64,0,32,0,16,0L0,0Z">
                </path>
            </svg>
            <div class="container">
                <div class="w-full px-4">
                    <div class="mx-auto mb-16 max-w-xl text-center">
                        <h2 class="mb-4 text-3xl font-bold text-dark dark:text-white sm:text-4xl lg:text-5xl">My
                            Project</h2>
                        <p class="text-md font-medium text-secondary md:text-lg text-slate-300">
                            lihat project saya sebelumnya
                        </p>
                        <!-- <div v-for="card in card" :key="card.id" class="card ">
                            <img :src="card.cover" class="card-img-top" :alt="card.nama">
                        </div> -->

                    </div>
                </div>
                

                <div class="flex w-full flex-wrap justify-center px-4 xl:mx-auto xl:w-10/12">
                    <div class="mb-12 p-4 md:w-1/2">
                        <div class="flex justify-center">
                            <NuxtLink to="/project/"
                                class="text-white font-semibold border border-white py-2 px-5 hover:px-6 rounded-full inline-flex items-center group transform hover:text-primary hover:-translate-y-1 duration-200">
                                View All Projects
                                <svg class="w-4 h-4 ml-1 transform group-hover:translate-x-2 duration-200" fill="none"
                                    stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                        d="M14 5l7 7m0 0l-7 7m7-7H3"></path>
                                </svg>
                            </NuxtLink>
                        </div>
                    </div>
                </div>
            </div>
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
                <path fill="#27272a" fill-opacity="1"
                    d="M0,192L11.4,170.7C22.9,149,46,107,69,90.7C91.4,75,114,85,137,106.7C160,128,183,160,206,165.3C228.6,171,251,149,274,154.7C297.1,160,320,192,343,181.3C365.7,171,389,117,411,96C434.3,75,457,85,480,85.3C502.9,85,526,75,549,96C571.4,117,594,171,617,181.3C640,192,663,160,686,170.7C708.6,181,731,235,754,266.7C777.1,299,800,309,823,288C845.7,267,869,213,891,192C914.3,171,937,181,960,197.3C982.9,213,1006,235,1029,218.7C1051.4,203,1074,149,1097,117.3C1120,85,1143,75,1166,96C1188.6,117,1211,171,1234,160C1257.1,149,1280,75,1303,58.7C1325.7,43,1349,85,1371,122.7C1394.3,160,1417,192,1429,208L1440,224L1440,320L1428.6,320C1417.1,320,1394,320,1371,320C1348.6,320,1326,320,1303,320C1280,320,1257,320,1234,320C1211.4,320,1189,320,1166,320C1142.9,320,1120,320,1097,320C1074.3,320,1051,320,1029,320C1005.7,320,983,320,960,320C937.1,320,914,320,891,320C868.6,320,846,320,823,320C800,320,777,320,754,320C731.4,320,709,320,686,320C662.9,320,640,320,617,320C594.3,320,571,320,549,320C525.7,320,503,320,480,320C457.1,320,434,320,411,320C388.6,320,366,320,343,320C320,320,297,320,274,320C251.4,320,229,320,206,320C182.9,320,160,320,137,320C114.3,320,91,320,69,320C45.7,320,23,320,11,320L0,320Z">
                </path>
            </svg>
        </section>
        <!-- project n -->

        <!-- contact -->
        <Contect />
        <Footer />
    </div>
</template>

<script setup>
// const client = useSupabaseClient()
// const card = ref([])

// async function getProducts() {
// const { data, error } = await client
// .from('card')
// .select()
// if(data) {
// card.value = data
// }
// }

// onMounted(() => {
// getProducts()
// })
</script>

<style scoped>
#project {
    background-image: url(@/assets/image/bg1.jpg);
}
</style>