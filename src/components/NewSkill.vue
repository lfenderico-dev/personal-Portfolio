<template>
  <div class="flex flex-row items-center gap-2 border-2 p-2 pr-4 hover:bg-black/30">
    <img class="size-10 lg:size-14 2xl:size-16" :src="imgSrc" />
    <h1 class="text-[12px] sm:text-sm md:text-lg">{{ skillName }}</h1>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  imgSrc: string
  skillName: string
}>()
</script>

<style scoped></style>
