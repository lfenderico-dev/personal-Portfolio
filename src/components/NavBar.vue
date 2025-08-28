<template>
  <div
    class="flex flex-row gap-2 bg-black text-white text-sm md:text-lg 2xl:text-2xl rounded-full w-fit mx-auto px-2 py-2 xl font-bold"
  >
    <button
      @click="selected = 'AboutMe'"
      class="rounded-full p-2"
      :class="{ 'bg-white text-black': selected == 'AboutMe' || null }"
    >
      About
    </button>
    <button
      class="rounded-full p-2"
      :class="{ 'bg-white text-black': selected == 'Skills' }"
      @click="selected = 'Skills'"
    >
      Skills
    </button>
    <button
      class="rounded-full p-2"
      :class="{ 'bg-white text-black': selected == 'Projects' }"
      @click="selected = 'Projects'"
    >
      Projects
    </button>
    <button
      class="rounded-full p-2"
      :class="{ 'bg-white text-black': selected == 'Blog' }"
      @click="selected = 'Blog'"
    >
      Blog
    </button>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const selected = ref<string | null>(null)
</script>

<style scoped></style>
