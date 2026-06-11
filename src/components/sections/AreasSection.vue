<script setup lang="ts">
import { ref } from "vue";
import {
    ArrowUpRight,
    Scale,
    BriefcaseBusiness,
    Building2,
} from "lucide-vue-next";

const activeCard = ref(0);
const hoveredCard = ref<number | null>(null);

const isActive = (index: number) =>
    hoveredCard.value === index || activeCard.value === index;

const services = [
    {
        id: "01",
        title: "Direito Digital",
        description:
            "Defesa dos direitos e interesses em questões de direito digital.",
        icon: Scale,
    },
    {
        id: "02",
        title: "Direito Civil",
        description:
            "Atuação em contratos, indenizações, responsabilidade civil e obrigações.",
        icon: BriefcaseBusiness,
    },
    {
        id: "03",
        title: "Direito Empresarial",
        description:
            "Assessoria jurídica estratégica para empresas e empreendedores.",
        icon: Building2,
    },
];
</script>

<template>
    <section id="areas" class="bg-[#F4F1EB] py-6">
        <div class="mx-auto max-w-7xl px-2 lg:px-10">
            <hr
                class="my-3 h-px border-t-0 bg-transparent bg-linear-to-r from-transparent via-gray-300 to-transparent opacity-80" />

            <div class="my-20">
                <div class="mb-6 flex items-center gap-4">
                    <div class="h-px w-8 bg-black/20" />

                    <span class="text-xs uppercase tracking-[0.35em] text-zinc-600">
                        Áreas de Atuação
                    </span>
                </div>

                <h2 class="max-w-3xl text-[44px] font-bold leading-none text-[#020B21] lg:text-6xl">
                    Soluções jurídicas

                    <span class="font-serif font-medium italic tracking-tighter text-[#2958FF]">
                        para proteger seus direitos.
                    </span>
                </h2>
            </div>

            <div class="mt-24 grid grid-cols-1 border-t border-black/10 lg:grid-cols-3">
                <article v-for="(service, index) in services" :key="service.id" @mouseenter="hoveredCard = index"
                    @mouseleave="hoveredCard = null" @click="activeCard = index"
                    class="group cursor-pointer flex min-h-80 px-6 flex-col justify-between border-b py-10 transition-all duration-300 lg:border-b-0 lg:border-r lg:px-10"
                    :class="isActive(index)
                            ? 'bg-[#020B21] border-[#020B21]'
                            : 'border-black/10'
                        ">
                    <div>
                        <div class="mb-10 flex h-14 w-14 items-center justify-center border transition-all duration-300"
                            :class="isActive(index)
                                    ? 'bg-[#2958FF] border-white/30'
                                    : 'border-black/10'
                                ">
                            <component :is="service.icon" :size="22" class="transition-colors duration-300" :class="isActive(index)
                                    ? 'text-white'
                                    : 'text-[#020B21]'
                                " />
                        </div>

                        <h3 class="mb-4 text-3xl font-semibold transition-colors duration-300" :class="isActive(index)
                                ? 'text-white'
                                : 'text-[#020B21]'
                            ">
                            {{ service.title }}
                        </h3>

                        <p class="max-w-sm leading-relaxed transition-colors duration-300" :class="isActive(index)
                                ? 'text-white/90'
                                : 'text-zinc-600'
                            ">
                            {{ service.description }}
                        </p>
                    </div>

                    <div class="mt-12 flex items-center justify-between">
                        <span class="text-sm transition-colors duration-300" :class="isActive(index)
                                ? 'text-white/70'
                                : 'text-zinc-400'
                            ">
                            {{ service.id }}
                        </span>

                        <ArrowUpRight :size="22" class="transition-all duration-300" :class="isActive(index)
                                ? 'text-white translate-x-1 -translate-y-1'
                                : 'text-[#020B21]'
                            " />
                    </div>
                </article>
            </div>
        </div>
    </section>
</template>