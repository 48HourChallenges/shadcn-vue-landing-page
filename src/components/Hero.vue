<script setup lang="ts">
import { useColorMode } from "@vueuse/core";
const mode = useColorMode();

import { Badge } from "@/components/ui/badge";
import { Button } from "@/components/ui/button";
import { ArrowRight } from "lucide-vue-next";
</script>

<template>
  <section class="bg-[#002611] text-white">
    <div class="container mx-auto px-4 py-20">
      <div class="max-w-[650px] space-y-6">
        <p class="text-[#4ADE80]">The 3PL in China trusted by 150+ Brands</p>
        
        <h1 class="text-5xl md:text-6xl font-semibold leading-tight">
          The future of supply-chain has arrived.
        </h1>

        <p class="text-lg text-gray-300 leading-relaxed">
          Ship globally within 1 day post-production, increase margins, and turn cash flow into profit with smart fulfillment. With Ecomflow, you tap into the best of both worlds: all the benefits of China fulfillment, without the downsides.
        </p>

        <div class="pt-4">
          <Button class="bg-[#4ADE80] hover:bg-[#4ADE80]/90 text-black px-8 py-6 text-lg font-medium">
            Work with us
          </Button>
        </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mt-20 max-w-[600px]">
        <div class="space-y-2">
          <div class="text-4xl font-semibold">3-10 Days</div>
          <div class="text-gray-400">Worldwide Delivery</div>
        </div>
        <div class="space-y-2">
          <div class="text-4xl font-semibold">99.8%</div>
          <div class="text-gray-400">Order Accuracy</div>
        </div>
        <div class="space-y-2">
          <div class="text-4xl font-semibold">75%</div>
          <div class="text-gray-400">Faster Lead Times</div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
</style>
