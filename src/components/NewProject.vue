<template>
  <div class="flex flex-col lg:flex-row gap-12 p-4">
    <div class="flex flex-col gap-8 lg:w-[75%]">
      <div class="flex flex-col gap-4">
        <div class="flex flex-col sm:flex-row gap-2 lg:gap-6 2xl:text-lg md:items-center">
          <div class="bg-neutral-400/70 w-fit px-4 rounded-full">{{ tag1 }}</div>
          <div class="bg-neutral-400/70 w-fit px-4 rounded-full">{{ tag2 }}</div>
        </div>
        <div class="flex flex-col sm:flex-row gap-2 lg:gap-6 2xl:text-lg md:items-center">
          <div class="bg-neutral-400/70 w-fit px-4 rounded-full">{{ tag3 }}</div>
          <div class="bg-neutral-400/70 w-fit px-4 rounded-full">{{ tag4 }}</div>
        </div>
      </div>

      <h1 class="text-3xl sm:text-4xl 2xl:text-5xl font-bold">{{ Title }}</h1>
      <p class="text-sm 2xl:text-lg text-neutral-700">{{ Description }}</p>

      <div class="flex flex-row gap-6 2xl:text-xl">
        <a class="px-4 py-2 bg-black text-white rounded-2xl flex items-center" :href="siteLink"
          ><i class="fa-solid fa-up-right-from-square text-sm 2xl:text-lg"></i> Live site</a
        >
        <a class="px-4 py-2 flex items-center" :href="githubLink"
          ><i class="fa-brands fa-github text-sm 2xl:text-lg"></i> Github</a
        >
      </div>

      <h1 class="text-sm 2xl:text-lg text-neutral-700">Year: {{ Year }}</h1>
    </div>

    <div class="flex items-center">
      <img class="size-max object-fill rounded-xl" :src="projectImg" />
    </div>
  </div>
  <hr class="w-full mx-auto border-1 bg-black my-10" />
</template>

<script setup lang="ts">
defineProps<{
  tag1?: string
  tag2?: string
  tag3?: string
  tag4?: string
  Title: string
  Description: string
  siteLink: string
  githubLink: string
  Year: number
  projectImg: string
}>()
</script>

<style scoped></style>
