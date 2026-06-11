<script setup lang="ts">
import { Motion } from "motion-v";
import { ArrowRight, Scale, Phone } from "lucide-vue-next";
</script>

<template>
  <section class="relative h-full overflow-hidden bg-[#F4F1EB] pt-44 md:pt-20 pb-16">
    <div class="mx-auto grid max-w-7xl items-center gap-20 px-4 lg:grid-cols-2 lg:px-8">
      <div>
        <Motion :initial="{ opacity: 0, y: 40 }" :animate="{ opacity: 1, y: 0 }" :transition="{ duration: 0.8 }">
          <span class="mb-4 block text-xs uppercase tracking-[0.35em] text-zinc-600">
             Advocacia — Atendimento Especializado
          </span>
        </Motion>

        <Motion :initial="{ opacity: 0, y: 50 }" :animate="{ opacity: 1, y: 0 }" :transition="{ duration: 1 }">
          <h1 class="max-w-2xl md:w-3xl text-[44px] font-bold md:font-semibold leading-none text-[#020B21] lg:text-[65px]">
            Transformamos desafios jurídicos em

            <span class="font-medium italic text-[#2958FF]">
              segurança e confiança.
            </span>
          </h1>
        </Motion>

        <Motion :initial="{ opacity: 0 }" :animate="{ opacity: 1 }" :transition="{ delay: 0.4, duration: 1 }">
          <p class="mt-6 font-light max-w-xl text-lg md:text-xl leading-relaxed text-zinc-600">
            Atuamos com dedicação, estratégia e excelência para garantir 
            segurança jurídica em cada etapa da sua jornada.
          </p>
        </Motion>

        <Motion class="mt-10 flex gap-3" :initial="{ opacity: 0, y: 20 }" :animate="{ opacity: 1, y: 0 }"
          :transition="{ delay: 0.6 }">
          <button
            class="group flex items-center gap-2 whitespace-nowrap bg-[#020B21] hover:bg-[#2958FF] px-5 md:px-8  py-3.5 font-medium text-sm text-white transition duration-300">
            Áreas de Atuação
            <ArrowRight :size="17" class="transition-transform duration-300 group-hover:translate-x-1" />
          </button>

          <button
            class="whitespace-nowrap border border-black/10 hover:bg-[#020B21] transition duration-300 hover:text-white px-5 md:px-8 py-3.5 font-medium text-sm">
            Agendar Consulta
          </button>
        </Motion>
      </div>

      <Motion class="relative hidden h-175 lg:block" :initial="{ opacity: 0, scale: 0.9 }"
        :animate="{ opacity: 1, scale: 1 }" :transition="{ delay: 0.5, duration: 1 }">
        <div
          class="absolute inset-0 bg-[linear-gradient(rgba(0,0,0,0.04)_1px,transparent_1px),linear-gradient(90deg,rgba(0,0,0,0.04)_1px,transparent_1px)] bg-size-[24px_24px]" />

        <div class="absolute left-20 top-20 h-24 w-24 border border-zinc-400" />

        <div class="absolute left-32 top-32 h-24 w-24 border border-[#2958FF]" />

        <div class="absolute left-1/2 top-1/2 h-3 w-3 bg-[#2958FF]" />

        <div class="absolute bottom-8 right-0 h-40 w-40 border border-[#2958FF]" />

        <div class="absolute bottom-0 right-0 h-40 w-40 bg-[#020B21]" />
      </Motion>
    </div>
  </section>
</template>