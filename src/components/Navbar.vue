<script lang="ts" setup>
import { ref } from "vue";

import { useColorMode } from "@vueuse/core";
const mode = useColorMode({
  initialValue: 'light',
  storageKey: 'color-mode'
});

import {
  NavigationMenu,
  NavigationMenuContent,
  NavigationMenuItem,
  NavigationMenuLink,
  NavigationMenuList,
  NavigationMenuTrigger,
} from "@/components/ui/navigation-menu";
import {
  Sheet,
  SheetContent,
  SheetHeader,
  SheetTitle,
  SheetTrigger,
} from "@/components/ui/sheet";

import { Button } from "@/components/ui/button";

import { ChevronsDown, Menu } from "lucide-vue-next";
import GithubIcon from "@/icons/GithubIcon.vue";
import ToggleTheme from "./ToggleTheme.vue";

interface RouteProps {
  href: string;
  label: string;
}

interface FeatureProps {
  title: string;
  description: string;
}

const routeList: RouteProps[] = [
  {
    href: "#testimonials",
    label: "Testimonials",
  },
  {
    href: "#team",
    label: "Team",
  },
  {
    href: "#contact",
    label: "Contact",
  },
  {
    href: "#faq",
    label: "FAQ",
  },
];

const featureList: FeatureProps[] = [
  {
    title: "Showcase Your Value ",
    description: "Highlight how your product solves user problems.",
  },
  {
    title: "Build Trust",
    description:
      "Leverages social proof elements to establish trust and credibility.",
  },
  {
    title: "Capture Leads",
    description:
      "Make your lead capture form visually appealing and strategically.",
  },
];

const isOpen = ref<boolean>(false);

const navItems = [
  // { label: "Benefits", href: "#benefits" },
  // { label: "Partners", href: "#partners" },
];
</script>

<template>
  <header class="bg-[#002611] border-b border-[#1a3d2a]">
    <nav class="container mx-auto px-4 py-4 flex justify-between items-center">
      <div class="flex items-center space-x-12">
        <!-- Logo -->
        <a href="/" class="flex items-center">
          <span class="text-[#4ADE80] text-2xl font-bold">AvSync</span>
        </a>

        <!-- Desktop Navigation -->
        <div class="hidden lg:flex items-center space-x-8">
          <a
            v-for="item in navItems"
            :key="item.label"
            :href="item.href"
            class="text-gray-300 hover:text-white transition-colors"
          >
            {{ item.label }}
          </a>
        </div>
      </div>

      <!-- CTA Button -->
      <Button class="bg-[#4ADE80] hover:bg-[#4ADE80]/90 text-black px-6 py-2 font-medium">
        Work with us
      </Button>
    </nav>
  </header>
</template>

<style scoped>
.shadow-light {
  box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.085);
}

.shadow-dark {
  box-shadow: inset 0 0 5px rgba(255, 255, 255, 0.141);
}
</style>
