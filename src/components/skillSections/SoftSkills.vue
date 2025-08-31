<template>
  <div class="grid grid-cols-2 gap-4 lg:grid-cols-3 2xl:grid-cols-4">
    <NewSkill
      v-for="softSkill in softSkills"
      :key="softSkill.key"
      :imgSrc="softSkill.imgSrc"
      :skillName="softSkill.skillName"
    />
  </div>
</template>

<script setup lang="ts">
import NewSkill from '../NewSkill.vue'

import problemSolvingIcon from '@/assets/photo/skillsIcons/softSkillsIcon/problemSolvingIcon.webp'
import teamWorkIcon from '@/assets/photo/skillsIcons/softSkillsIcon/teamWorkIcon.webp'
import documentingIcon from '@/assets/photo/skillsIcons/softSkillsIcon/documentingIcon.webp'
import teachingIcon from '@/assets/photo/skillsIcons/softSkillsIcon/teachingIcon.webp'

const softSkills = [
  {
    key: 1,
    imgSrc: problemSolvingIcon,
    skillName: 'Problem solving',
  },
  {
    key: 2,
    imgSrc: teamWorkIcon,
    skillName: 'Teamwork',
  },
  {
    key: 3,
    imgSrc: documentingIcon,
    skillName: 'Documenting',
  },
  {
    key: 4,
    imgSrc: teachingIcon,
    skillName: 'Teaching',
  },
]
</script>

<style scoped></style>
