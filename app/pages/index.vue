<script setup lang="ts">
import Search from "@/components/Search.vue";
import { Skeleton } from "@/components/ui/skeleton";
</script>

<template>
  <Search />
  <main class="max-h-screen pt-4 flex flex-1 flex-col gap-4">
    <div class="grid auto-rows-min gap-4 md:grid-cols-3">
      <Skeleton class="bg-muted/50 aspect-video" />
      <Skeleton class="bg-muted/50 aspect-video" />
      <Skeleton class="bg-muted/50 aspect-video" />
    </div>
    <Skeleton class="bg-muted/50 min-h-screen flex-1 md:min-h-min" />
  </main>
</template>
