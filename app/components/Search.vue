<script setup lang="ts">
import { Input } from "@/components/ui/input";
import { Search } from "lucide-vue-next";
</script>

<template>
  <div class="relative">
    <Search class="absolute top-2 left-2 text-muted-foreground size-5" />
    <Input
      class="pl-9 bg-accent border-none "
      type="text"
      placeholder="Search..."
    />
  </div>
</template>
