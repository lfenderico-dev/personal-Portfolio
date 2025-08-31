<template>
  <div class="grid grid-cols-2 gap-4 lg:grid-cols-3 2xl:grid-cols-4">
    <NewSkill
      :key="tool.key"
      v-for="tool in tools"
      :img-src="tool.imgSrc"
      :skillName="tool.skillName"
    />
  </div>
</template>

<script setup lang="ts">
import NewSkill from '../NewSkill.vue'

import hashcatIcon from '@/assets/photo/skillsIcons/toolsIcon/hashcat-icon.webp'
import aircrackIcon from '@/assets/photo/skillsIcons/toolsIcon/aircrack-ngIcon.webp'
import reconNgIcon from '@/assets/photo/skillsIcons/toolsIcon/reconNg.webp'
import sherlockIcon from '@/assets/photo/skillsIcons/toolsIcon/SherlockIcon.webp'
import wiresharkIcon from '@/assets/photo/skillsIcons/toolsIcon/wireshark-icon.webp'

const tools = [
  {
    key: 1,
    imgSrc: wiresharkIcon,
    skillName: 'Wireshark',
  },
  {
    key: 2,
    imgSrc: aircrackIcon,
    skillName: 'Aircrack-ng',
  },
  {
    key: 3,
    imgSrc: hashcatIcon,
    skillName: 'Hashcat',
  },
  {
    key: 4,
    imgSrc: reconNgIcon,
    skillName: 'Recon-ng',
  },
  {
    key: 5,
    imgSrc: sherlockIcon,
    skillName: 'Sherlock',
  },
]
</script>

<style scoped></style>
