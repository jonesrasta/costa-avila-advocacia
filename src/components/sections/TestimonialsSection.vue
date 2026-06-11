<script setup lang="ts">
import { ref } from "vue";
import { Motion } from "motion-v";
import { Quote, ArrowUpRight } from "lucide-vue-next";

const activeTestimonial = ref(0);

const testimonials = [
  {
    name: "João Martins",
    role: "Empresário",
    text: "Recebi um atendimento extremamente profissional e transparente. O suporte jurídico foi essencial para a segurança do meu negócio.",
  },
  {
    name: "Fernanda Costa",
    role: "Cliente",
    text: "Equipe altamente qualificada e comprometida. Sempre me senti segura durante todo o processo.",
  },
  {
    name: "Carlos Almeida",
    role: "Empresário",
    text: "A atenção aos detalhes e a dedicação do escritório fizeram toda a diferença na resolução do meu caso.",
  },
];
</script>

<template>
  <section id="depoimentos" class="bg-[#F4F1EB] py-14">
    <div class="mx-auto max-w-7xl px-2.5 lg:px-10">
      <Motion
        class="mb-20"
        :initial="{ opacity: 0, y: 40 }"
        :while-in-view="{ opacity: 1, y: 0 }"
        :transition="{ duration: 0.7 }"
        :in-view-options="{ once: true }"
      >
        <div class="mb-6 flex items-center gap-4">
          <div class="h-px w-8 bg-black/20" />

          <span class="text-xs uppercase tracking-[0.35em] text-zinc-600">
            Depoimentos
          </span>
        </div>

        <h2
          class="max-w-3xl text-[44px] lg:text-6xl font-bold tracking-tighter leading-none text-[#020B21]"
        >
          A confiança dos nossos clientes

          <span
            class="font-medium tracking-tighter font-serif italic text-[#2958FF]"
          >
            é o nosso maior resultado.
          </span>
        </h2>
      </Motion>

      <div class="grid border-t border-black/10 lg:grid-cols-3">
        <Motion
          v-for="(testimonial, index) in testimonials"
          :key="testimonial.name"
          as="article"
          @mouseenter="activeTestimonial = index"
          :initial="{ opacity: 0, y: 50 }"
          :while-in-view="{ opacity: 1, y: 0 }"
          :transition="{
            duration: 0.6,
            delay: index * 0.15,
          }"
          :in-view-options="{ once: true }"
          :while-hover="{ y: -6 }"
          class="flex min-h-95 flex-col justify-between border-b py-10 px-5 transition-all duration-300 lg:border-b-0 lg:border-r lg:px-10"
          :class="
            activeTestimonial === index
              ? 'bg-[#020B21] border-[#020B21]'
              : 'border-black/10 hover:bg-[#020B21] hover:border-[#020B21]'
          "
        >
          <div>
            <Quote
              :size="32"
              class="mb-8 transition-colors duration-300"
              :class="
                activeTestimonial === index
                  ? 'text-white'
                  : 'text-[#2958FF]'
              "
            />

            <p
              class="text-lg leading-relaxed transition-colors duration-300"
              :class="
                activeTestimonial === index
                  ? 'text-white/90'
                  : 'text-zinc-600'
              "
            >
              "{{ testimonial.text }}"
            </p>
          </div>

          <div class="mt-12">
            <div class="flex items-center justify-between">
              <div>
                <h3
                  class="text-xl font-semibold transition-colors duration-300"
                  :class="
                    activeTestimonial === index
                      ? 'text-white'
                      : 'text-[#020B21]'
                  "
                >
                  {{ testimonial.name }}
                </h3>

                <p
                  class="mt-1 text-sm transition-colors duration-300"
                  :class="
                    activeTestimonial === index
                      ? 'text-white/70'
                      : 'text-zinc-500'
                  "
                >
                  {{ testimonial.role }}
                </p>
              </div>

              <ArrowUpRight
                :size="22"
                class="transition-all duration-300"
                :class="
                  activeTestimonial === index
                    ? 'text-white translate-x-1 -translate-y-1'
                    : 'text-[#020B21]'
                "
              />
            </div>
          </div>
        </Motion>
      </div>
    </div>
  </section>
</template>