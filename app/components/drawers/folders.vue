<script setup lang="ts"></script>

<template>
  <ul class="space-y-4">
    <li v-for="_ in 10" class="space-y-2">
      <div class="grid grid-cols-3 gap-0.5">
        <img
          src="https://i.pinimg.com/1200x/2f/de/dc/2fdedc3dc7e149b54b7c884367fd9663.jpg"
          alt="Nugraha Jati Utama"
          class="col-span-2 row-span-2 object-cover h-full"
        />
        <img
          src="https://i.pinimg.com/1200x/4c/7d/b4/4c7db43074edf877d9ffb64d8ac1616d.jpg"
          alt="Playdate"
          class="row-span-1 object-cover h-full"
        />
        <img
          src="https://i.pinimg.com/1200x/8a/8e/8e/8a8e8e6662c311fa816a709357c8323d.jpg"
          alt="Lists Material Design 3"
          class="row-span-1 object-cover h-full"
        />
      </div>
      <div>
        <h2>Design</h2>
        <small>5 pins</small>
      </div>
    </li>
  </ul>
</template>