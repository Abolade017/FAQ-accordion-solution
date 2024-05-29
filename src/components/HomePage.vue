<script setup lang="ts">
import FaqCard from "./FAQCard.vue";
</script>

<template>
  <div class="h-screen bg-light-pink">
    <div class="hidden md:block">
      <img
        src="/background-pattern-desktop.svg"
        alt="desktop background image"
        srcset=""
        class="w-full"
      />
    </div>
    <div class="block md:hidden">
      <img
        src="/background-pattern-mobile.svg"
        alt="mobile background image"
        srcset=""
        class="w-full"
      />
    </div>
    <div class="flex justify-center items-center md:mx-0 mx-6">
      <FaqCard class="-mt-28"></FaqCard>
    </div>
  </div>
</template>
