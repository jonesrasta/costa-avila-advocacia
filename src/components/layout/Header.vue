<script setup lang="ts">
import logo from "@/assets/costa-logo.svg";
import { ArrowRight } from "lucide-vue-next";

const menuItems = [
  "Áreas de Atuação",
  "O Escritório",
  "Advogados",
  "Depoimentos",
  "Contato",
];
</script>

<template>
  <header class="fixed top-0 left-0 z-50 w-full border-b border-black/10 bg-[#F4F1EB]">
    <div class="mx-auto flex h-18 max-w-7xl items-center justify-between px-2 lg:px-10">
      <img :src="logo" alt="Costa Advocacia" class="h-12 w-auto shrink-0" />

      <nav class="hidden md:block">
        <ul class="flex gap-8">
          <li v-for="item in menuItems" :key="item">
            <a href="#" class="text-sm text-zinc-600 transition hover:text-black">
              {{ item }}
            </a>
          </li>
        </ul>
      </nav>
      <button
        class="group flex items-center bg-[#020B21] gap-2 hover:bg-[#2958FF] px-7 py-3.5 font-medium text-sm text-white transition duration-300">
        Falar Conosco
        <ArrowRight :size="17" class="transition-transform duration-300 group-hover:translate-x-1" />
      </button>
    </div>
  </header>
</template>