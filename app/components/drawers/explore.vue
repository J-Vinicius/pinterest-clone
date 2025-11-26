<script setup lang="ts"></script>
<template>
  <header class="p-2">
    <h2 class="text-xl font-medium">Inspire-se</h2>
    <small class="text-xs text-muted-foreground">
      17 de novembro de 2025
    </small>
  </header>
  <ul class="space-y-2">
    <li v-for="_ in 10" class="relative max-h-24 overflow-hidden">
      <img
        src="https://i.pinimg.com/736x/d0/de/24/d0de24af870e21f8b3d92c799e1955ed.jpg"
        alt="Carrosel White and Black"
        class="object-cover object-center opacity-75"
      />
      <div class="absolute bottom-2 inset-x-2">
        <small>Fotografia e desenhos</small>
        <h3>Preto e branco aesthetic</h3>
      </div>
    </li>
  </ul>
</template>
