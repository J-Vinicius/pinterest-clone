<script setup lang="ts">
import { Plus, UserPlus } from "lucide-vue-next";
import { Button } from "../ui/button";
</script>

<template>
  <div class="flex flex-col gap-4 p-4">
    <Button>
      <Plus />
      Nova Mensagem
    </Button>
    <Button variant="outline" class="flex flex-col h-fit">
      <UserPlus />
      Convidar seus amigos
      <small class="text-muted-foreground">Conecte-se para começar a conversar</small>
    </Button>
  </div>
</template>
