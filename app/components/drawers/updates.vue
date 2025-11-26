<script setup lang="ts">
import {
  Item,
  ItemContent,
  ItemDescription,
  ItemGroup,
  ItemMedia,
  ItemTitle,
} from "@/components/ui/item";
import { Search } from "lucide-vue-next";
</script>

<template>
  <div class="flex w-full max-w-md flex-col gap-6">
    <ItemGroup class="gap-4">
      <Item v-for="_ in 10" :key="_" as-child role="listitem">
        <a href="#">
          <ItemMedia variant="icon">
            <Search />
          </ItemMedia>
          <ItemContent>
            <ItemTitle class="line-clamp-2"> Ainda está procurando? </ItemTitle>
            <ItemDescription>
              Explore ideias relacionadas a <b>Truque de Cartas</b>
            </ItemDescription>
          </ItemContent>
          <ItemContent class="flex-none text-center">
            <ItemDescription>2 sem</ItemDescription>
          </ItemContent>
        </a>
      </Item>
    </ItemGroup>
  </div>
</template>
