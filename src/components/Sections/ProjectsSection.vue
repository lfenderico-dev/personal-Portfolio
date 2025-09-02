<template>
  <div class="h-fit flex flex-col gap-4 my-[10%] mx-[10%] lg:mx-[5%] lg:my-[15%]">
    <div class="flex flex-row items-center gap-4">
      <hr class="border-1 rounded-full inline w-[20%] bg-black" />
      <h1
        class="text-xl sm:text-2xl md:text-3xl lg:text-4xl xl:text-5xl 2xl:text-6xl text-center font-bold w-fit inline"
      >
        My works
      </h1>
    </div>

    <div>
      <NewProject v-for="project in projects" :key="project.id" v-bind="project" />
    </div>
  </div>
</template>

<script setup lang="ts">
import NewProject from '../NewProject.vue'

import sliceDiceImg from '@/assets/photo/projectImg/slice&DiceImg.webp'

const projects = [
  {
    id: 1,
    tag1: 'VueJs',
    tag2: 'Tailwindcss',
    tag3: 'Typescript',
    tag4: 'Landing page',
    Title: 'Slice&Dice',
    Description:
      'Slice and Dice is a pizza restaurant that makes fresh, delicious pizzas with bold flavors. Visit our website to check out the menu, order online, and see our latest deals. Great pizza is just a click away!',
    siteLink: 'https://sliceanddice-pizza.netlify.app/',
    githubLink: 'https://github.com/lfenderico-dev/Slice-Dice.git',
    Year: 2025,
    projectImg: sliceDiceImg,
  },
]
</script>

<style scoped></style>
