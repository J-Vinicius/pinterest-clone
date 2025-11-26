<script setup lang="ts">
import Sidebar from "~/components/Sidebar.vue";
import { SidebarInset, SidebarProvider } from "~/components/ui/sidebar";
</script>

<template>
  <SidebarProvider
    :style="{
      '--sidebar-width': '25rem',
    }"
  >
    <Sidebar />
    <SidebarInset>
      <slot />
    </SidebarInset>
  </SidebarProvider>
</template>
