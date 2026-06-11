<script setup lang="ts">
import logo from "@/assets/costa-logo-white.svg";
import { ArrowUpRight, Instagram, MessageCircle } from "lucide-vue-next";
import { Icon } from "@iconify/vue";

</script>

<template>
    <footer id="footer" class="bg-[#020B21] text-white">
        <!-- CTA -->
        <section class="mx-auto max-w-7xl px-6 py-18 md:py-24 lg:px-10">
            <div class="flex flex-col gap-12 pb-18 md:pb-24 lg:flex-row lg:items-center lg:justify-between">
                <div>
                    <div class="mb-6 flex items-center gap-4">
                        <div class="h-px w-10 bg-[#2958FF]/40"></div>

                        <span class="text-xs uppercase tracking-[0.35em] text-white/60">
                            Contato
                        </span>
                    </div>

                    <h2 class="max-w-2xl text-4xl font-bold tracking-tighter leading-none lg:text-6xl">
                        Transforme desafios jurídicos
                        <span class="font-light font-serif tracking-tighter italic text-[#2958FF]">
                            em decisões mais seguras.
                        </span>
                    </h2>
                </div>

                <div class="flex flex-col gap-4 min-w-[320px]">
                    <a href="#"
                        class="group flex items-center justify-between bg-[#F4F1EB] px-6 py-4 text-[#020B21] transition-all hover:translate-x-1">
                        <div class="flex items-center gap-3">
                            <Icon icon="iconoir:message-solid" width="17" height="17" />
                            <span class="font-medium">WhatsApp</span>
                        </div>

                        <ArrowUpRight :size="18"
                            class="transition-transform group-hover:-translate-y-1 group-hover:translate-x-1" />
                    </a>

                    <a href="#"
                        class="group flex items-center justify-between border border-white/10 px-6 py-4 transition-all hover:border-white/30">
                        <div class="flex items-center gap-3">
                            <Instagram :size="18" />
                            <span class="font-medium">Instagram</span>
                        </div>

                        <ArrowUpRight :size="18"
                            class="transition-transform group-hover:-translate-y-1 group-hover:translate-x-1" />
                    </a>
                </div>
            </div>
            <div class="h-px bg-linear-to-r from-transparent via-white/20 to-transparent"></div>
        </section>

        <!-- Footer -->
        <section class="mx-auto max-w-7xl px-6 pb-8 lg:px-10">
            <div class="grid gap-14 lg:grid-cols-3">

                <!-- Marca -->
                <div>
                    <a href="#inicio">
                        <img :src="logo" alt="Costa Advocacia" class="h-16 md:h-18 w-auto shrink-0 mb-4 -mt-8 md:mt-0" />
                    </a>
                    <p class="max-w-xs text-white/70 leading-relaxed">
                        Estamos prontos para oferecer o suporte jurídico que você precisa.
                    </p>

                </div>

                <!-- Navegação -->
                <div>
                    <h4 class="mb-6 text-xs uppercase tracking-[0.3em] text-white/50">
                        Navegação
                    </h4>

                    <ul class="space-y-4 text-white/80">
                        <li class="transition duration-300 hover:text-[#2958FF]"><a href="#inicio">Ínicio</a></li>
                        <li class="transition duration-300 hover:text-[#2958FF]"><a href="#areas">Áreas de Atuação</a></li>
                        <li class="transition duration-300 hover:text-[#2958FF]"><a href="#escritorio">O Escritório</a></li>
                        <li class="transition duration-300 hover:text-[#2958FF]"><a href="#advogados">Advogados</a></li>
                        <li class="transition duration-300 hover:text-[#2958FF]"><a href="#depoimentos">Depoimentos</a></li>
                        <li class="transition duration-300 hover:text-[#2958FF]"><a href="#contato">Contato</a></li>
                    </ul>
                </div>

                <!-- Redes -->
                <div>
                    <h4 class="mb-6 text-xs uppercase tracking-[0.3em] text-white/50">
                        Redes
                    </h4>

                    <ul class="space-y-4 text-white/80 mb-6">
                        <li class="transition duration-300 hover:text-[#2958FF]"><a href="#">Instagram</a></li>
                        <li class="transition duration-300 hover:text-[#2958FF]"><a href="#">WhatsApp</a></li>
                        <li class="transition duration-300 hover:text-[#2958FF]"><a href="#">Email</a></li>
                    </ul>
                </div>
            </div>

            <!-- Bottom -->
            <div class="mt-8">
                <div class="h-px bg-linear-to-r from-transparent via-white/20 to-transparent" />

                <div
                    class="flex flex-col gap-4 pt-8 text-sm text-white/50 lg:flex-row lg:items-center lg:justify-between">
                    <span>
                        © 2026 Costa & Avila Advocacia. Todos os direitos reservados.
                    </span>

                    <span class="font-medium tracking-wide text-white/70">
                        Segurança • Estratégia • Resultado
                    </span>
                </div>
            </div>
        </section>
    </footer>
</template>