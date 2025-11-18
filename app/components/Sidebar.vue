<script setup lang="ts">
import { h, ref } from "vue";
import {
  Bell,
  Compass,
  Folders,
  MessageSquare,
  Pin,
  PlusSquare,
  Settings,
} from "lucide-vue-next";
import {
  Sidebar,
  SidebarHeader,
  SidebarMenuButton,
  SidebarMenuItem,
  SidebarTrigger,
  useSidebar,
  type SidebarProps,
} from "./ui/sidebar";
import NavUser from "./NavUser.vue";
import New from "./drawers/new.vue";
import Updates from "./drawers/updates.vue";

const props = withDefaults(defineProps<SidebarProps>(), {
  collapsible: "icon",
});

const menus = [
  {
    icon: Compass,
    title: "Explore",
    isActive: false,
  },
  {
    icon: Folders,
    title: "Folders",
    isActive: false,
  },
  {
    icon: PlusSquare,
    title: "New",
    isActive: false,
  },
  {
    icon: Bell,
    title: "Updates",
    isActive: false,
  },
  {
    icon: MessageSquare,
    title: "Messages",
    isActive: false,
  },
];

const activeItem = ref(menus[0]);
const { setOpen } = useSidebar();
</script>

<template>
  <Sidebar
    class="overflow-hidden *:data-[sidebar=sidebar]:flex-row"
    v-bind="props"
  >
    <Sidebar
      collapsible="none"
      class="w-[calc(var(--sidebar-width-icon)+1px)]! border-r"
    >
      <SidebarHeader>
        <SidebarMenuItem>
          <SidebarMenuButton size="lg" as-child class="md:h-8 md:p-0">
            <NuxtLink to="/">
              <div
                class="bg-sidebar-primary text-sidebar-primary-foreground flex aspect-square size-8 items-center justify-center rounded-lg"
              >
                <Pin class="size-4" />
              </div>
              <div class="grid flex-1 text-left text-sm leading-tight">
                <span class="truncate font-semibold">Pinterest</span>
                <span class="truncate text-xs"
                  >A better design for Pinterest</span
                >
              </div>
            </NuxtLink>
          </SidebarMenuButton>
        </SidebarMenuItem>
      </SidebarHeader>
      <SidebarContent>
        <SidebarGroup>
          <SidebarGroupContent class="px-1.5 md:px-0">
            <SidebarMenu>
              <SidebarMenuItem v-for="menu in menus" :key="menu.title">
                <SidebarMenuButton
                  :tooltip="h('div', { hidden: false }, menu.title)"
                  :is-active="activeItem?.title === menu.title"
                  class="px-2.5 md:px-2"
                  @click="
                    () => {
                      activeItem = menu;
                      setOpen(true);
                    }
                  "
                >
                  <component :is="menu.icon" />
                  <span>{{ menu.title }}</span>
                </SidebarMenuButton>
              </SidebarMenuItem>
            </SidebarMenu>
          </SidebarGroupContent>
        </SidebarGroup>
      </SidebarContent>
      <SidebarFooter class="p-0 gap-0">
        <SidebarGroup>
          <SidebarGroupContent class="px-1.5 md:px-0">
            <SidebarMenu>
              <SidebarMenuItem>
                <SidebarMenuButton
                  class="px-2.5 md:px-2"
                  :tooltip="h('div', { hidden: false }, 'Settings')"
                >
                  <Settings />
                </SidebarMenuButton>
              </SidebarMenuItem>
            </SidebarMenu>
          </SidebarGroupContent>
        </SidebarGroup>
        <div class="p-2">
          <NavUser
            name="J-Vinicius"
            email="jorgeviniciusmoreiralucas@gmail.com"
            avatar="https://github.com/J-Vinicius.png"
          />
        </div>
      </SidebarFooter>
    </Sidebar>
    <Sidebar collapsible="none" class="hidden flex-1 md:flex">
      <SidebarHeader class="gap-3.5 border-b p-4">
        <div class="flex w-full items-center justify-between">
          <div class="text-base font-medium text-foreground">
            {{ activeItem?.title }}
          </div>
          <SidebarTrigger />
        </div>
      </SidebarHeader>
      <SidebarContent class="">
        <Updates />
      </SidebarContent>
    </Sidebar>
  </Sidebar>
</template>
