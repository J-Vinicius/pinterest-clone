<script setup lang="ts">
import {
  Folder,
  Pin,
  ScissorsSquareDashedBottom,
} from "lucide-vue-next";
import {
  Item,
  ItemContent,
  ItemDescription,
  ItemMedia,
  ItemTitle,
} from "@/components/ui/item";

const newActions = [
  {
    title: "Pin",
    desc: "Publique suas fotos ou vídeos e adicione links, adesivos, efeitos e muito mais",
    icon: Pin,
  },
  {
    title: "Pasta",
    desc: "Organize uma coleção dos seus Pins favoritos criando uma pasta",
    icon: Folder,
  },
  {
    title: "Colagem",
    desc: "Junte e combine suas ideias para criar sua visão e criar algo novo",
    icon: ScissorsSquareDashedBottom,
  },
];
</script>

<template>
  <div class="flex w-full max-w-lg flex-col gap-6">
    <Item v-for="action in newActions" variant="muted" class="hover:bg-muted cursor-pointer">
      <ItemMedia variant="icon">
        <component :is="action.icon" />
      </ItemMedia>
      <ItemContent>
        <ItemTitle>{{ action.title }}</ItemTitle>
        <ItemDescription class="line-clamp-none">
          {{ action.desc }}
        </ItemDescription>
      </ItemContent>
    </Item>
  </div>
</template>
