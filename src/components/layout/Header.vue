<script setup lang="ts">
import logo from "@/assets/costa-logo.svg";
import { ArrowRight } from "lucide-vue-next";

const menuItems = [
  { label: "Ínicio", href: "#inicio" },
  { label: "Áreas de Atuação", href: "#areas" },
  { label: "Escritório", href: "#escritorio" },
  { label: "Advogados", href: "#advogados" },
  { label: "Depoimentos", href: "#depoimentos" },
  { label: "Contato", href: "#contato" },
];
</script>

<template>
  <header class="fixed mx-auto top-0 left-0 z-50 w-full border-b border-black/10 bg-[#F4F1EB] overflow-hidden">
    <div class="flex h-20 max-w-7xl items-center justify-between md:mx-auto mx-2 lg:px-10">
      <a href="#inicio">
        <img :src="logo" alt="Costa Advocacia" class="h-13 md:h-16 w-auto shrink-0" />
      </a>

      <nav class="hidden md:block">
        <ul class="flex gap-8">
          <li v-for="item in menuItems" :key="item.label">
            <a :href="item.href" class="text-sm text-zinc-600 transition hover:text-black">
              {{ item.label }}
            </a>
          </li>
        </ul>
      </nav>
      <a href="#footer"
        class="group flex items-center bg-[#020B21] gap-2 hover:bg-[#2958FF] px-3.5 py-3.5 md:px-7 md:py-3.5 font-medium text-sm text-white transition duration-300">
        Falar Conosco
        <ArrowRight :size="17" class="transition-transform duration-300 group-hover:translate-x-1" />
      </a>
    </div>
  </header>
</template>