<template>
    <div id="main" class="bg-[#27272a]">
        <Header />
        <section class="pt-24 pb-10 ">
            <h4 class="text-center font-semibold text-white text-3xl ">Lets See My Project</h4>
            <p class="text-center font-medium text-base text-slate-300">These are some of the projects I've made</p>
            <!-- <p v-if="loading" class="custom-loader m-auto text-center"></p> -->
            <template>


</template>


</section>
</div>
<Footer />
</template>

<script setup>
// const loading = ref(true)
// const getDatas = async () => {
//     loading.value = true
//     const { data, error } = await supabase.from("projects").select()
//         .order("id", { ascending: false })
//         .range(0, 5)
//         .limit(6)
//     datas.value = data

//     loading.value = false
//     gsap.fromTo(
//         projects.value,
//         { opacity: 0 },
//         { opacity: 1, duration: 4, ease: 'power2.out' }
//     )
// }
onMounted(() => {
    getDatas()







})
</script>

<style>
.custom-loader {
    width: 45px;
    height: 40px;
    --c: linear-gradient(#facc15 0 0);
    background:
        var(--c) 0% 100%,
        var(--c) 50% 100%,
        var(--c) 100% 100%;
    background-size: 9px 100%;
    background-repeat: no-repeat;
    animation: b2 1s infinite linear;
}

@keyframes b2 {
    20% {
        background-size: 9px 60%, 9px 100%, 9px 100%
    }

    40% {
        background-size: 9px 80%, 9px 60%, 9px 100%
    }

    60% {
        background-size: 9px 100%, 9px 80%, 9px 60%
    }

    80% {
        background-size: 9px 100%, 9px 100%, 9px 80%
    }
}
</style>