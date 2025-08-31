<template>
  <div class="grid grid-cols-2 gap-4 lg:grid-cols-3 2xl:grid-cols-4">
    <NewSkill
      v-for="devSkill in devSkills"
      :key="devSkill.key"
      :imgSrc="devSkill.imgSrc"
      :skillName="devSkill.skillName"
    />
  </div>
</template>

<script setup lang="ts">
import NewSkill from '../NewSkill.vue'

import htmlIcon from '@/assets/photo/skillsIcons/WebDevIcon/htmlIcon.webp'
import cssIcon from '@/assets/photo/skillsIcons/WebDevIcon/cssIcon.webp'
import twCSSIcon from '@/assets/photo/skillsIcons/WebDevIcon/twCSSIcon.webp'
import jsIcon from '@/assets/photo/skillsIcons/WebDevIcon/JSIcon.webp'
import tsIcon from '@/assets/photo/skillsIcons/WebDevIcon/TsIcon.webp'
import vueIcon from '@/assets/photo/skillsIcons/WebDevIcon/VueJsIcon.webp'

const devSkills = [
  {
    key: 1,
    imgSrc: htmlIcon,
    skillName: 'HTML',
  },
  {
    key: 2,
    imgSrc: cssIcon,
    skillName: 'CSS',
  },
  {
    key: 3,
    imgSrc: twCSSIcon,
    skillName: 'TailwindCSS',
  },
  {
    key: 4,
    imgSrc: jsIcon,
    skillName: 'Javascript',
  },
  {
    key: 5,
    imgSrc: tsIcon,
    skillName: 'Typescript',
  },
  {
    key: 6,
    imgSrc: vueIcon,
    skillName: 'VueJs',
  },
]
</script>

<style scoped></style>
