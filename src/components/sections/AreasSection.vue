<script setup lang="ts">
import {
    ArrowUpRight,
    Scale,
    BriefcaseBusiness,
    Building2,
} from "lucide-vue-next";

const services = [
    {
        id: "01",
        title: "Direito Trabalhista",
        description:
            "Defesa dos direitos de trabalhadores e empresas em questões trabalhistas.",
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
        <div class="mx-auto max-w-7xl px-6 lg:px-10">
            <hr className="h-px border-t-0 bg-transparent bg-linear-to-r from-transparent via-gray-300 to-transparent opacity-80 my-2.5 md:my-3" />
            <div class="mb-20 my-20">
                <div class="flex items-center gap-4 mb-6">
                    <div class="h-px w-8 bg-black/20" />

                    <span class="text-xs uppercase tracking-[0.35em] text-zinc-600">
                        Áreas de Atuação
                    </span>
                </div>

                <h2 class="max-w-3xl text-[44px] lg:text-6xl font-bold leading-none text-[#020B21]">
                    Soluções jurídicas <span class="font-light text-[#2958FF] italic">para proteger seus
                        direitos.</span>
                </h2>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-3">
                <article v-for="service in services" :key="service.id"
                    class="group flex min-h-80 flex-col justify-between border-b border-black/10 py-10 transition-all duration-300 hover:bg-[#020B21] hover:border-[#020B21] lg:border-b-0 lg:border-r lg:px-10">
                    <div>
                        <div
                            class="mb-10 flex h-14 w-14 items-center justify-center border border-black/10 group-hover:bg-[#2958FF] hover:border-gray-200 transition-colors duration-300 group-hover:border-white/30">
                            <component :is="service.icon" :size="22"
                                class="text-[#020B21] transition-colors duration-300 group-hover:text-white" />
                        </div>

                        <h3
                            class="mb-4 text-3xl font-semibold text-[#020B21] transition-colors duration-300 group-hover:text-white">
                            {{ service.title }}
                        </h3>

                        <p
                            class="max-w-sm leading-relaxed text-zinc-600 transition-colors duration-300 group-hover:text-white/90">
                            {{ service.description }}
                        </p>
                    </div>

                    <div class="mt-12 flex items-center justify-between">
                        <span class="text-sm text-zinc-400 transition-colors duration-300 group-hover:text-white/70">
                            {{ service.id }}
                        </span>

                        <ArrowUpRight :size="22"
                            class="transition-all duration-300 group-hover:text-white group-hover:-translate-y-1 group-hover:translate-x-1" />
                    </div>
                </article>
            </div>
        </div>
    </section>
</template>