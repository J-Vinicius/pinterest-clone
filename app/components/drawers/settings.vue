<script setup lang="ts">
import { ExternalLinkIcon } from "lucide-vue-next";
import { Item, ItemActions, ItemGroup } from "../ui/item";
import Separator from "../ui/separator/Separator.vue";

const settings = {
  geral: [
    { title: "Configurações", href: "#" },
    { title: "Refinar suas recomendações", href: "#" },
    { title: "Link para o Pinterest", href: "#" },
    { title: "Central de Denúncias e Violações", href: "#" },
    { title: "Instalar o aplicativo do Windows", href: "#" },
    {
      title: "Participe do programa de testes Beta",
      href: "#",
      external: true,
    },
  ],

  support: [
    { title: "Central de Ajuda", href: "#", external: true },
    { title: "Criar widget", href: "#", external: true },
    { title: "Remoções", href: "#", external: true },
    { title: "Anúncios personalizados", href: "#" },
    { title: "Seus direitos de privacidade", href: "#" },
    { title: "Política de Privacidade", href: "#", external: true },
    { title: "Termos de Serviço", href: "#", external: true },
  ],
};

const recursos = [
  { title: "Sobre", href: "#" },
  { title: "Imprensa", href: "#" },
  { title: "Empresas", href: "#" },
  { title: "Carreiras", href: "#" },
  { title: "Desenvolvedores", href: "#" },
];
</script>

<template>
  <ul class="space-y-4">
    <li>
      <ItemGroup>
        <Item v-for="setting in settings.geral" as-child>
          <NuxtLink
            :to="setting.href"
            target="_blank"
            rel="noopener noreferrer"
          >
            <ItemContent>
              <ItemTitle>{{ setting.title }}</ItemTitle>
            </ItemContent>
            <ItemActions v-if="setting.external">
              <ExternalLinkIcon class="size-4" />
            </ItemActions>
          </NuxtLink>
        </Item>
      </ItemGroup>
    </li>
    <li>
      <small class="text-muted-foreground p-4">Suporte</small>
      <ItemGroup>
        <Item v-for="setting in settings.support" as-child>
          <NuxtLink
            :to="setting.href"
            target="_blank"
            rel="noopener noreferrer"
          >
            <ItemContent>
              <ItemTitle>{{ setting.title }}</ItemTitle>
            </ItemContent>
            <ItemActions v-if="setting.external">
              <ExternalLinkIcon class="size-4" />
            </ItemActions>
          </NuxtLink>
        </Item>
      </ItemGroup>
    </li>
    <li class="p-4">
      <small>Recursos</small>
      <ul class="flex flex-wrap gap-3">
        <li v-for="recurso in recursos">
          <NuxtLink :to="recurso.href">{{ recurso.title }}</NuxtLink>
        </li>
      </ul>
    </li>
  </ul>
</template>
