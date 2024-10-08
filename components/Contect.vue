<template>
    <section id="contact" class="pt-28 pb-32 bg-[#27272a]">
      <div class="container">
        <div class="w-full px-4">
          <div class="mx-auto mb-16 max-w-xl text-center">
            <h2 class="mb-4 text-3xl font-bold text-white sm:text-4xl lg:text-5xl">Kontak Saya Disini</h2>
            <p class="text-md font-medium text-slate-300 md:text-lg">jika ingin berinteraksi dengan saya, apapun akan saya bahas.^^</p>
          </div>
        </div>

        <form>
          <div class="w-full lg:mx-auto lg:w-2/3">
            <div class="mb-8 w-full px-4">
              <label for="name" class="text-base font-bold text-[#facc15]">Nama</label>
              <input type="text" id="name" class="w-full rounded-md bg-white p-3 text-dark focus:border-[#facc15] focus:outline-none focus:ring-1 focus:ring-[#facc15]" />
            </div>
            <div class="mb-8 w-full px-4">
              <label for="email" class="text-base font-bold text-[#facc15]">Email</label>
              <input type="email" id="email" class="w-full rounded-md bg-white p-3 text-dark focus:border-[#facc15] focus:outline-none focus:ring-1 focus:ring-[#facc15]" />
            </div>
            <div class="mb-8 w-full px-4">
              <label for="message" class="text-base font-bold text-[#facc15]">Pesan</label>
              <textarea type="email" id="email" class="h-32 w-full rounded-md bg-white p-3 text-dark focus:border-[#facc15] focus:outline-none focus:ring-1 focus:ring-[#facc15]"></textarea>
            </div>
            <div class="w-full px-4">
              <button class="w-full rounded-full bg-[#fdba74] py-3 px-8 text-base font-semibold text-white transition duration-500 hover:opacity-80 hover:shadow-lg">Kirim</button>
            </div>
          </div>
        </form>
      </div>
    </section>
</template>