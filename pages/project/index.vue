<template>
    <div id="main" class="bg-[#27272a]">
        <div class="pt-24 pb-10 ">
            <h4 class="text-center font-semibold text-white text-3xl ">Lets See My Project</h4>
            <p class="text-center font-medium text-base text-slate-300">These are some of the projects I've made</p>
            <Project />
        </div>
    </div>
</template>

<script setup>

</script>

<style scoped>
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