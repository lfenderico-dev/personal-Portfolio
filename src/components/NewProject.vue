<template>
  <div class="flex flex-col gap-12">
    <div class="flex flex-col gap-8">
      <div class="grid-cols-2 grid gap-2">
        <div class="bg-neutral-400/70 w-fit px-8 rounded-full">{{ tag1 }}</div>
        <div class="bg-neutral-400/70 w-fit px-8 rounded-full">{{ tag2 }}</div>
        <div class="bg-neutral-400/70 w-fit px-8 rounded-full">{{ tag3 }}</div>
      </div>

      <h1 class="text-3xl font-bold">{{ Title }}</h1>
      <p>{{ Description }}</p>

      <div class="flex flex-row">
        <a :href="siteLink">Live site</a>
        <a :href="githubLink">Github</a>
      </div>

      <h1>Year: {{ Year }}</h1>
    </div>

    <div>
      <img :src="projectImg" />
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  tag1?: string
  tag2?: string
  tag3?: string
  Title: string
  Description: string
  siteLink: string
  githubLink: string
  Year: number
  projectImg: string
}>()
</script>

<style scoped></style>
