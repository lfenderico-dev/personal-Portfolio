<template>
  <div
    class="flex flex-row gap-2 bg-black text-white text-sm md:text-lg 2xl:text-2xl rounded-full w-fit mx-auto px-2 py-2 xl font-bold"
  >
    <button
      @click="((selected = 'About'), sendToParent())"
      class="rounded-full p-2"
      :class="{ 'bg-white text-black': selected == 'About' || null }"
    >
      About
    </button>
    <button
      class="rounded-full p-2"
      :class="{ 'bg-white text-black': selected == 'Skills' }"
      @click="((selected = 'Skills'), sendToParent())"
    >
      Skills
    </button>
    <button
      class="rounded-full p-2"
      :class="{ 'bg-white text-black': selected == 'Projects' }"
      @click="((selected = 'Projects'), sendToParent())"
    >
      Projects
    </button>
    <button
      class="rounded-full p-2"
      :class="{ 'bg-white text-black': selected == 'Blog' }"
      @click="((selected = 'Blog'), sendToParent())"
    >
      Blog
    </button>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const emit = defineEmits(['selection'])

const selected = ref<string | null>(null)

const sendToParent = () => {
  emit('selection', selected.value)
}
</script>

<style scoped></style>
