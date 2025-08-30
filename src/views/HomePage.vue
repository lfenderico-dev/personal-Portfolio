<template>
  <div>
    <h1 class="text-center mx-auto my-8 text-xl md:text-2xl 2xl:text-3xl font-bold">
      <i class="fa-solid fa-at"></i>Lorenzo - Fenderico
    </h1>
    <NavBar @selection="handleSelection" />

    <div
      class="flex flex-col lg:flex-row my-[10%] mx-[10%] lg:mx-[5%] lg:my-[5%] gap-2 lg:gap-14 items-center"
    >
      <div class="flex flex-col gap-6 xl:gap-10 lg:w-[50%] p-4">
        <h1 class="text-5xl lg:text-7xl xl:text-8xl 2xl:text-9xl text-left font-bold">
          Pentester/ Developer
        </h1>
        <div class="flex flex-col bg-black p-8 gap-2 rounded-xl lg:w-[100%]">
          <div class="flex flex-row gap-2 text-sm 2xl:text-lg">
            <i class="fa-solid fa-circle text-red-500"></i>
            <i class="fa-solid fa-circle text-yellow-500"></i>
            <i class="fa-solid fa-circle text-green-500"></i>
          </div>
          <span class="text-white text-sm xl:text-lg 2xl:text-xl"
            ><strong class="text-emerald-500">computer: ~$ </strong>Greetings, fellow humans!
            <i class="fa-solid fa-face-smile-wink text-yellow-500 text-lg"></i
          ></span>
        </div>
        <div class="flex flex-row text-3xl lg:text-4xl xl:text-5xl gap-4">
          <i class="fa-brands fa-square-github"></i>
          <i class="fa-brands fa-square-linkedin"></i>
          <i class="fa-brands fa-square-x-twitter"></i>
        </div>
      </div>
      <img
        src="@/assets/photo/computerSprite.svg"
        class="size-75 lg:size-90 xl:size-120 2xl:size-160 object-cover mx-auto my-[5%] lg:my-auto"
      />
    </div>
  </div>

  <AboutSection v-if="currentlySelected == 'About'" />
  <SkillsSection v-if="currentlySelected == 'Skills'" />
  <ProjectsSection v-if="currentlySelected == 'Projects'" />
  <BlogSection v-if="currentlySelected == 'Blog'" />
</template>

<script setup lang="ts">
import NavBar from '@/components/NavBar.vue'
import AboutSection from '@/components/Sections/AboutSection.vue'
import BlogSection from '@/components/Sections/BlogSection.vue'
import ProjectsSection from '@/components/Sections/ProjectsSection.vue'
import SkillsSection from '@/components/Sections/SkillsSection.vue'
import { ref } from 'vue'

const currentlySelected = ref<string | null>(null)

const handleSelection = (selection: string) => {
  currentlySelected.value = selection
  console.log(currentlySelected.value)
}
</script>

<style scoped></style>
