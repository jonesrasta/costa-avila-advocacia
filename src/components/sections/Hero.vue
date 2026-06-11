<script setup lang="ts">
import { Motion } from "motion-v";
import { ArrowRight } from "lucide-vue-next";
</script>

<template>
  <section id="inicio" class="relative h-full overflow-x-hidden bg-[#F4F1EB] pt-44 md:pt-20 pb-16">

    <!-- Imagem mobile: visível só abaixo de lg, posicionada atrás (z-0) -->
    <Motion class="absolute inset-y-0 overflow-hidden right-0 w-2/3 lg:hidden z-0 pointer-events-none" :initial="{ opacity: 0, x: 100 }"
      :animate="{ opacity: 1, x: 0 }" :transition="{ delay: 0.5, duration: 1 }">
      <div class="absolute inset-0 bg-[linear-gradient(rgba(0,0,0,0.04)_1px,transparent_1px),linear-gradient(90deg,rgba(0,0,0,0.04)_1px,transparent_1px)] bg-size-[60px_60px] -mt-4" />
      <img src="@/assets/lady-justice.webp" alt="" class="w-full h-full object-cover object-left mt-20" />
      <div class="absolute inset-0 bg-linear-to-r from-[#F4F1EB] via-[#F4F1EB]/75 to-transparent" />
    </Motion>

    <div class="mx-auto grid max-w-7xl items-center gap-20 px-4 lg:grid-cols-2 lg:px-10">
      <!-- Conteúdo com z-10 para ficar na frente da imagem mobile -->
      <div class="relative z-10">
        <Motion class="overflow-hidden" :initial="{ opacity: 0, y: 40 }" :animate="{ opacity: 1, y: 0 }"
          :transition="{ duration: 0.8 }">
          <span class="mb-4 block text-xs md:text-sm uppercase tracking-[0.35em] text-[#020B21] md:-mt-20">
            Advocacia <span class="text-[#020B21]/65"> • </span> Atendimento Especializado
          </span>
        </Motion>

        <Motion :initial="{ opacity: 0, y: 50 }" :animate="{ opacity: 1, y: 0 }" :transition="{ duration: 1 }">
          <h1
            class="max-w-172.5 text-[44px] font-bold md:font-semibold leading-none text-[#020B21] lg:text-[65px] md:-mt-20">
            Transformamos desafios jurídicos em
            <span class="font-medium font-serif tracking-tighter italic text-[#2958FF]">
              segurança e confiança.
            </span>
          </h1>
        </Motion>

        <Motion class="overflow-hidden" :initial="{ opacity: 0 }" :animate="{ opacity: 1 }"
          :transition="{ delay: 0.4, duration: 1 }">
          <p class="mt-6 font-light max-w-xl text-lg md:text-xl leading-relaxed text-zinc-900">
            Atuamos com dedicação, estratégia e excelência para garantir
            segurança jurídica em cada etapa da sua jornada.
          </p>
        </Motion>

        <Motion class="mt-10 flex gap-3 overflow-hidden" :initial="{ opacity: 0, y: 20 }"
          :animate="{ opacity: 1, y: 0 }" :transition="{ delay: 0.6 }">
          <a href="#areas"
            class="group flex items-center gap-2 whitespace-nowrap bg-[#020B21] hover:bg-[#2958FF] px-5 md:px-8 py-3.5 font-medium text-sm text-white transition duration-300">
            Áreas de Atuação
            <ArrowRight :size="17" class="transition-transform duration-300 group-hover:translate-x-1" />
          </a>
          <a href="#contato"
            class="whitespace-nowrap border bg-[#f4f1eb] border-black/10 hover:bg-[#020B21] transition duration-300 hover:text-white px-5 md:px-8 py-3.5 font-medium text-sm">
            Agendar Consulta
          </a>
        </Motion>
      </div>

      <!-- Imagem desktop: coluna direita, visível só em lg+ -->
      <Motion class="relative hidden h-215 lg:block overflow-hidden" :initial="{ opacity: 0, scale: 0.9 }"
        :animate="{ opacity: 1, scale: 1 }" :transition="{ delay: 0.5, duration: 1 }">
        <div
          class="absolute inset-0 bg-[linear-gradient(rgba(0,0,0,0.04)_1px,transparent_1px),linear-gradient(90deg,rgba(0,0,0,0.04)_1px,transparent_1px)] bg-size-[60px_60px] -mt-4" />
        <img src="@/assets/lady-justice.webp" alt="Lady Justice"
          class="absolute inset-0 w-full h-full object-cover z-10" />
        <!-- <div class="absolute left-20 top-20 h-24 w-24 border border-zinc-400" />

        <div class="absolute left-32 top-32 h-24 w-24 border border-[#2958FF]" /> -->

        <!-- <div class="absolute left-1/2 top-1/2 h-3 w-3 bg-[#2958FF]" /> -->

        <!-- <div class="absolute bottom-8 right-0 h-40 w-40 border border-[#2958FF]" />

        <div class="absolute bottom-0 right-0 h-40 w-40 bg-[#020B21]" /> -->
      </Motion>
    </div>
  </section>
</template>