<template>
  <div class="grid grid-cols-2 gap-4 lg:grid-cols-3 2xl:grid-cols-4">
    <NewSkill
      v-for="programmingLanguage in ProgrammingLanguages"
      :key="programmingLanguage.key"
      :imgSrc="programmingLanguage.imgSrc"
      :skillName="programmingLanguage.skillName"
    />
  </div>
</template>

<script setup lang="ts">
import NewSkill from '../NewSkill.vue'

import jsIcon from '@/assets/photo/skillsIcons/WebDevIcon/JSIcon.webp'
import tsIcon from '@/assets/photo/skillsIcons/WebDevIcon/TsIcon.webp'
import pythonIcon from '@/assets/photo/skillsIcons/ProgrammingLanguages/pythonIcon.webp'

const ProgrammingLanguages = [
  {
    key: 1,
    imgSrc: jsIcon,
    skillName: 'Javascript',
  },
  {
    key: 2,
    imgSrc: tsIcon,
    skillName: 'Typescript',
  },
  {
    key: 3,
    imgSrc: pythonIcon,
    skillName: 'Python',
  },
]
</script>

<style scoped></style>
