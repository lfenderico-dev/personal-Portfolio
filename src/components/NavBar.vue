<template>
  <div class="sticky top-0 z-50 my-4">
    <div
      class="flex flex-row gap-2 bg-white/50 backdrop-blur-md border-b border-white/20 text-black text-sm md:text-lg 2xl:text-2xl w-full px-2 py-2 xl font-bold justify-center"
    >
      <button
        class="rounded-xl p-2 px-4"
        @click="((selected = 'About'), scrollToSection('About'))"
        :class="{ 'bg-black text-white': selected == 'About' }"
      >
        About
      </button>
      <button
        class="rounded-xl p-2 px-4"
        @click="((selected = 'Skills'), scrollToSection('Skills'))"
        :class="{ 'bg-black text-white': selected == 'Skills' }"
      >
        Skills
      </button>
      <button
        class="rounded-xl p-2 px-4"
        @click="((selected = 'Projects'), scrollToSection('Projects'))"
        :class="{ 'bg-black text-white': selected == 'Projects' }"
      >
        Projects
      </button>
      <button
        class="rounded-xl p-2 px-4"
        @click="((selected = 'Blog'), scrollToSection('Blog'))"
        :class="{ 'bg-black text-white': selected == 'Blog' }"
      >
        Blog
      </button>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const selected = ref<null | string>(null)

const scrollToSection = (id: string) => {
  document.getElementById(id)?.scrollIntoView({ behavior: 'smooth' })
}
</script>

<style scoped></style>
