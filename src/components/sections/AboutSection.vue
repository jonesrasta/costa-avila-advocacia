<script setup lang="ts">
import { Motion } from "motion-v";
</script>

<template>
  <section id="escritorio" class="bg-[#F4F1EB] py-24 md:py-40">
    <div class="mx-auto max-w-7xl px-6 lg:px-10">
      <div class="grid gap-20 lg:grid-cols-2">
        <!-- Left -->
        <Motion
          :initial="{ opacity: 0, y: 40 }"
          :while-in-view="{ opacity: 1, y: 0 }"
          :transition="{ duration: 0.7 }"
          :in-view-options="{ once: true }"
        >
          <div class="flex items-center gap-4 mb-6">
            <div class="h-px w-8 bg-black/20" />

            <span
              class="text-xs uppercase tracking-[0.35em] text-zinc-600"
            >
              Sobre o Escritório
            </span>
          </div>

          <h2
            class="max-w-xl text-[44px] lg:text-6xl font-bold tracking-tight md:tracking-normal leading-none text-[#020B21]"
          >
            Experiência jurídica
            <span class="font-medium tracking-tighter font-serif italic text-[#2958FF]">
              com foco em resultados
            </span>
            e segurança.
          </h2>
        </Motion>

        <!-- Right -->
        <Motion
          :initial="{ opacity: 0, y: 40 }"
          :while-in-view="{ opacity: 1, y: 0 }"
          :transition="{ duration: 0.7, delay: 0.2 }"
          :in-view-options="{ once: true }"
        >
          <p class="text-lg leading-relaxed text-zinc-600">
            Nosso escritório atua com excelência na prestação de
            serviços jurídicos, oferecendo soluções estratégicas
            e atendimento personalizado para pessoas físicas e
            empresas.

            Trabalhamos com ética, transparência e compromisso,
            buscando sempre a melhor defesa dos interesses de
            nossos clientes.
          </p>
        </Motion>
      </div>

      <!-- Stats -->
      <div
        class="mt-24 grid border-t border-black/10 lg:grid-cols-3"
      >
        <Motion
          class="border-b border-black/10 py-10 lg:border-b-0 lg:border-r lg:px-10"
          :initial="{ opacity: 0, y: 30 }"
          :while-in-view="{ opacity: 1, y: 0 }"
          :transition="{ delay: 0.1 }"
          :in-view-options="{ once: true }"
        >
          <h3 class="text-5xl lg:text-6xl font-semibold text-[#020B21]">
            15+
          </h3>

          <p class="mt-3 text-zinc-600">
            Anos de experiência jurídica.
          </p>
        </Motion>

        <Motion
          class="border-b border-black/10 py-10 lg:border-b-0 lg:border-r lg:px-10"
          :initial="{ opacity: 0, y: 30 }"
          :while-in-view="{ opacity: 1, y: 0 }"
          :transition="{ delay: 0.2 }"
          :in-view-options="{ once: true }"
        >
          <h3 class="text-5xl lg:text-6xl  font-semibold text-[#020B21]">
            500+
          </h3>

          <p class="mt-3 text-zinc-600">
            Casos atendidos com dedicação.
          </p>
        </Motion>

        <Motion
          class="py-10 lg:px-10"
          :initial="{ opacity: 0, y: 30 }"
          :while-in-view="{ opacity: 1, y: 0 }"
          :transition="{ delay: 0.3 }"
          :in-view-options="{ once: true }"
        >
          <h3 class="text-5xl lg:text-6xl font-semibold text-[#020B21]">
            98%
          </h3>

          <p class="mt-3 text-zinc-600">
            Índice de satisfação dos clientes.
          </p>
        </Motion>
      </div>
    </div>
  </section>
</template>