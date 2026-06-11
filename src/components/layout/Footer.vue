<script setup lang="ts">
import logo from "@/assets/costa-logo-white.svg";
import { ArrowUpRight, Instagram, MessageCircle } from "lucide-vue-next";
</script>

<template>
    <footer id="footer" class="bg-[#020B21] text-white">
        <!-- CTA -->
        <section class="mx-auto max-w-7xl px-6 py-24 lg:px-10">
            <div
                class="flex flex-col gap-12 border-b border-white/10 pb-24 lg:flex-row lg:items-center lg:justify-between">
                <div>
                    <div class="mb-6 flex items-center gap-4">
                        <div class="h-px w-10 bg-white/20"></div>

                        <span class="text-xs uppercase tracking-[0.35em] text-white/60">
                            Contato
                        </span>
                    </div>

                    <h2 class="max-w-2xl text-4xl font-bold leading-none lg:text-6xl">
                        Transforme desafios jurídicos
                        <span class="italic font-light text-[#2958FF]">
                            em decisões mais seguras.
                        </span>
                    </h2>
                </div>

                <div class="flex flex-col gap-4 min-w-[320px]">
                    <a href="#"
                        class="group flex items-center justify-between bg-[#F4F1EB] px-6 py-5 text-[#020B21] transition-all hover:translate-x-1">
                        <div class="flex items-center gap-3">
                            <MessageCircle :size="17" />
                            <span class="font-medium">WhatsApp</span>
                        </div>

                        <ArrowUpRight :size="18"
                            class="transition-transform group-hover:-translate-y-1 group-hover:translate-x-1" />
                    </a>

                    <a href="#"
                        class="group flex items-center justify-between border border-white/10 px-6 py-5 transition-all hover:border-white/30">
                        <div class="flex items-center gap-3">
                            <Instagram :size="18" />
                            <span class="font-medium">Instagram</span>
                        </div>

                        <ArrowUpRight :size="18"
                            class="transition-transform group-hover:-translate-y-1 group-hover:translate-x-1" />
                    </a>
                </div>
            </div>
        </section>

        <!-- Footer -->
        <section class="mx-auto max-w-7xl px-6 pb-8 lg:px-10">
            <div class="grid gap-14 py-4 lg:grid-cols-3">
                
                <!-- Marca -->
                <div>
                    <a href="#inicio">
                        <img :src="logo" alt="Costa Advocacia" class="h-14 w-auto shrink-0 mb-4" />
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
                        <li><a href="#areas">Áreas de Atuação</a></li>
                        <li><a href="#escritorio">O Escritório</a></li>
                        <li><a href="#advogados">Advogados</a></li>
                        <li><a href="#depoimentos">Depoimentos</a></li>
                        <li><a href="#contato">Contato</a></li>
                    </ul>
                </div>

                <!-- Redes -->
                <div>
                    <h4 class="mb-6 text-xs uppercase tracking-[0.3em] text-white/50">
                        Redes
                    </h4>

                    <ul class="space-y-4 text-white/80">
                        <li><a href="#">Instagram</a></li>
                        <li><a href="#">WhatsApp</a></li>
                        <li><a href="#">Email</a></li>
                    </ul>
                </div>
            </div>

            <!-- Bottom -->
            <div
                class="flex flex-col gap-4 border-t border-white/10 pt-8 text-sm text-white/50 lg:flex-row lg:items-center lg:justify-between">
                <span>
                    © 2026 Costa & Avila Advocacia. Todos os direitos reservados.
                </span>

                <span>
                    Segurança. Estratégia. Resultado.
                </span>
            </div>
        </section>
    </footer>
</template>