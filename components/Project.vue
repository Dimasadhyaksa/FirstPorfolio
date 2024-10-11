<template>
  <div class="pt-20 pb-10">
    <p v-if="loading" class="custom-loader m-auto text-center"></p>
    <div class="group portfolio flex flex-wrap mb-16 align-middle hover:no-underline focus:no-underline" v-for="project in project" :key="project.id">
      <!-- di gunain di page project -->
      <div class="w-full md:w-6/12 relative h-52 md:h-96 px-5">
        <img :src="project.image" class="absolute object-cover w-full h-full rounded-2xl transform duration-200 group-hover:-translate-y-2 group-hover:shadow-xl" />
      </div>
      <div class="w-full md:w-5/12 mt-5 md:mt-0 md:ml-10 self-center">
        <h3 class="text-2xl md:text-4xl font-normal leading-tight group-hover:underline text-white">
          {{ project.name }}
        </h3>
        <!-- <p class="mt-2 mb-4 text-base text-slate-500">{{ project.deskripsi }}</p> -->
        <!-- <div class="mt-5" ></div> -->
        <NuxtLink :to="`/project/` + project.id" class="mt-5 text-white inline-flex items-center group-hover:underline duration-200">
          View Project
          <svg class="w-4 h-4 ml-2 transform group-hover:translate-x-2 duration-200" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round">
            <path d="M5 12h14"></path>
            <path d="M12 5l7 7-7 7"></path>
          </svg>
        </NuxtLink>
      </div>
    </div>
    <!-- <div class="flex items-center justify-center">
    <button v-if="!datas.length < count && !load"
        class="rounded-full bg-blue-500 py-3 px-8 text-base font-semibold text-white transition duration-300 hover:bg-blue-400 hover:shadow-lg"
        @click="loadmore">
        More Project
    </button>
    <p v-if="!datas.length < count && load" class="custom-loader m-auto text-center"></p>
    </div> -->
  </div>
</template>

<script setup>
const supabase = useSupabaseClient();

const { data: project, error } = useAsyncData("project", async () => {
  const { data, error } = await supabase.from("projects").select("*");
  if (error) throw error;
  return data;
});
</script>
<style>
.custom-loader {
  width: 45px;
  height: 40px;
  --c: linear-gradient(#facc15 0 0);
  background: var(--c) 0% 100%, var(--c) 50% 100%, var(--c) 100% 100%;
  background-size: 9px 100%;
  background-repeat: no-repeat;
  animation: b2 1s infinite linear;
}

@keyframes b2 {
  20% {
    background-size: 9px 60%, 9px 100%, 9px 100%;
  }

  40% {
    background-size: 9px 80%, 9px 60%, 9px 100%;
  }

  60% {
    background-size: 9px 100%, 9px 80%, 9px 60%;
  }

  80% {
    background-size: 9px 100%, 9px 100%, 9px 80%;
  }
}
</style>
