<script setup lang="ts">
import { Motion } from "motion-v";
import { ArrowUpRight } from "lucide-vue-next";

const lawyers = [
  {
    name: "Camila Avila",
    role: "Direito Digital",
    image: "/teams/camila.webp",
  },
  {
    name: "Mariana Costa",
    role: "Direito Civil",
    image: "/teams/mariana.webp",
  },
  {
    name: "Ricardo Almeida",
    role: "Direito Empresarial",
    image: "/teams/ricardo.webp"
  },
];
</script>

<template>
  <section id="advogados" class="bg-[#F4F1EB] py-6 md:py-14">
    <div class="mx-auto max-w-7xl px-3 lg:px-10">
      <!-- Header -->
      <Motion
        class="mb-20"
        :initial="{ opacity: 0, y: 40 }"
        :while-in-view="{ opacity: 1, y: 0 }"
        :transition="{ duration: 0.7 }"
        :in-view-options="{ once: true }"
      >
        <div class="mb-6 flex items-center gap-4">
          <div class="h-px w-8 bg-black/20" />

          <span
            class="text-xs uppercase tracking-[0.35em] text-zinc-600"
          >
            Nossa Equipe
          </span>
        </div>

        <h2
          class="max-w-3xl text-[44px] lg:text-6xl font-bold tracking-tighter leading-none text-[#020B21]"
        >
          Profissionais comprometidos
          <span class="font-medium tracking-tighter font-serif italic text-[#2958FF]">
            com a excelência jurídica.
          </span>
        </h2>
      </Motion>

      <!-- Grid -->
      <div class="grid gap-0 border-t border-black/10 lg:grid-cols-3">
        <Motion
          v-for="(lawyer, index) in lawyers"
          :key="lawyer.name"
          as="article"
          :initial="{ opacity: 0, y: 50 }"
          :while-in-view="{ opacity: 1, y: 0 }"
          :transition="{
            duration: 0.6,
            delay: index * 0.15
          }"
          :in-view-options="{ once: true }"
          class="group border-b border-black/10 transition-all duration-300 hover:bg-[#020B21] hover:border-[#020B21] lg:border-b-0 lg:border-r "
        >
          <div class="overflow-hidden">
            <img
              :src="lawyer.image"
              :alt="lawyer.name"
              class="h- w-full object-cover md:grayscale transition duration-500 group-hover:scale-105 hover:grayscale-0"
            />
          </div>

          <div class="mt-8 px-4">
            <h3
              class="text-3xl font-semibold text-[#020B21] transition-colors duration-300 group-hover:text-white"
            >
              {{ lawyer.name }}
            </h3>

            <p
              class="mt-2 text-zinc-600 transition-colors duration-300 group-hover:text-white/80"
            >
              {{ lawyer.role }}
            </p>
          </div>

          <div class="mt-10 flex justify-end px-4 py-4">
            <ArrowUpRight
              :size="22"
              class="transition-all duration-300 group-hover:text-white group-hover:-translate-y-1 group-hover:translate-x-1"
            />
          </div>
        </Motion>
      </div>
    </div>
  </section>
</template>