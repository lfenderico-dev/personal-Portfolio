<template>
  <div class="grid grid-cols-2 gap-4 lg:grid-cols-3 2xl:grid-cols-4">
    <NewSkill
      v-for="language in languages"
      :key="language.key"
      :imgSrc="language.imgSrc"
      :skillName="language.skillName"
    />
  </div>
</template>

<script setup lang="ts">
import NewSkill from '../NewSkill.vue'

import italianFlag from '@/assets/photo/skillsIcons/LanguagesIcon/italyIcon.webp'
import englishFlag from '@/assets/photo/skillsIcons/LanguagesIcon/englishIcon.webp'
import germanFlag from '@/assets/photo/skillsIcons/LanguagesIcon/germanIcon.webp'

const languages = [
  {
    key: 1,
    imgSrc: italianFlag,
    skillName: 'Italian',
  },
  {
    key: 2,
    imgSrc: englishFlag,
    skillName: 'English',
  },
  {
    key: 3,
    imgSrc: germanFlag,
    skillName: 'German',
  },
]
</script>

<style scoped></style>
