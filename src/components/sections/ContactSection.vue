<script setup lang="ts">
import { Motion } from "motion-v";
import {
  Mail,
  Phone,
  MapPin,
  ArrowRight,
} from "lucide-vue-next";
</script>

<template>
  <section id="contato" class="bg-[#F4F1EB] py-14">
    <div class="mx-auto max-w-7xl px-6 lg:px-10">
      <!-- Header -->
      <Motion
        class="mb-20"
        :initial="{ opacity: 0, y: 40 }"
        :while-in-view="{ opacity: 1, y: 0 }"
        :transition="{ duration: 0.7 }"
        :in-view-options="{ once: true }"
      >
        <div class="mb-6 flex items-center gap-4">
          <div class="h-px w-8 bg-black/20" />

          <span
            class="text-xs uppercase tracking-[0.35em] text-zinc-600"
          >
            Contato
          </span>
        </div>

        <h2
          class="max-w-3xl text-[44px] lg:text-6xl font-bold leading-none text-[#020B21]"
        >
          Estamos prontos para
          <span class="font-medium tracking-tighter font-serif italic text-[#2958FF]">
            atender você.
          </span>
        </h2>
      </Motion>

      <div class="grid gap-16 lg:grid-cols-2">
        <!-- Informações -->
        <Motion
          :initial="{ opacity: 0, x: -40 }"
          :while-in-view="{ opacity: 1, x: 0 }"
          :transition="{ duration: 0.7 }"
          :in-view-options="{ once: true }"
        >
          <p
            class="max-w-lg text-lg leading-relaxed text-zinc-600"
          >
            Entre em contato para agendar uma consulta ou
            esclarecer dúvidas sobre nossos serviços jurídicos.
            Nossa equipe está pronta para oferecer o suporte
            necessário para o seu caso.
          </p>

          <div class="mt-12 space-y-8">
            <div class="flex items-start gap-4">
              <Phone
                :size="20"
                class="mt-1 text-[#2958FF]"
              />

              <div>
                <h3 class="font-semibold text-[#020B21]">
                  Telefone
                </h3>

                <p class="mt-1 text-zinc-600">
                  (11) 99999-9999
                </p>
              </div>
            </div>

            <div class="flex items-start gap-4">
              <Mail
                :size="20"
                class="mt-1 text-[#2958FF]"
              />

              <div>
                <h3 class="font-semibold text-[#020B21]">
                  E-mail
                </h3>

                <p class="mt-1 text-zinc-600">
                  contato@costaeavila.com.br
                </p>
              </div>
            </div>

            <div class="flex items-start gap-4">
              <MapPin
                :size="20"
                class="mt-1 text-[#2958FF]"
              />

              <div>
                <h3 class="font-semibold text-[#020B21]">
                  Endereço
                </h3>

                <p class="mt-1 text-zinc-600">
                  São Paulo • SP
                </p>
              </div>
            </div>
          </div>
        </Motion>

        <!-- Formulário -->
        <Motion
          :initial="{ opacity: 0, x: 40 }"
          :while-in-view="{ opacity: 1, x: 0 }"
          :transition="{ duration: 0.7, delay: 0.2 }"
          :in-view-options="{ once: true }"
        >
          <form
            class="border border-black/10 bg-white p-8 lg:p-10"
          >
            <div class="space-y-6">
              <div>
                <label
                  class="mb-2 block text-sm font-medium text-[#020B21]"
                >
                  Nome
                </label>

                <input
                  type="text"
                  class="w-full border border-black/10 px-4 py-3 outline-none transition focus:border-[#2958FF]"
                  placeholder="Seu nome"
                />
              </div>

              <div>
                <label
                  class="mb-2 block text-sm font-medium text-[#020B21]"
                >
                  E-mail
                </label>

                <input
                  type="email"
                  class="w-full border border-black/10 px-4 py-3 outline-none transition focus:border-[#2958FF]"
                  placeholder="seuemail@email.com"
                />
              </div>

              <div>
                <label
                  class="mb-2 block text-sm font-medium text-[#020B21]"
                >
                  Assunto
                </label>

                <input
                  type="text"
                  class="w-full border border-black/10 px-4 py-3 outline-none transition focus:border-[#2958FF]"
                  placeholder="Como podemos ajudar?"
                />
              </div>

              <div>
                <label
                  class="mb-2 block text-sm font-medium text-[#020B21]"
                >
                  Mensagem
                </label>

                <textarea
                  rows="5"
                  class="w-full resize-none border border-black/10 px-4 py-3 outline-none transition focus:border-[#2958FF]"
                  placeholder="Descreva sua necessidade..."
                />
              </div>

              <button
                type="submit"
                class="group flex items-center gap-2 bg-[#020B21] px-8 py-4 font-medium text-white transition duration-300 hover:bg-[#2958FF]"
              >
                Enviar Mensagem

                <ArrowRight
                  :size="18"
                  class="transition-transform duration-300 group-hover:translate-x-1"
                />
              </button>
            </div>
          </form>
        </Motion>
      </div>
    </div>
  </section>
</template>