<template>
  <div class="h-fit flex flex-col gap-4 my-[10%] mx-[10%] lg:mx-[5%] lg:my-[15%]">
    <div class="flex flex-row items-center gap-4">
      <hr class="border-1 rounded-full inline w-[20%] bg-black" />
      <h1
        class="text-xl sm:text-2xl md:text-3xl lg:text-4xl xl:text-5xl 2xl:text-6xl text-center font-bold w-fit inline"
      >
        Skills
      </h1>
    </div>

    <div class="overflow-x-auto w-full">
      <SkillsNavbar @skillset="handleSkillset" />
    </div>

    <div>
      <ToolsSection v-if="skillSelection == 'Tools' || skillSelection == null" />
      <WebDevSection v-if="skillSelection == 'Web development'" />
      <LanguagesSection v-if="skillSelection == 'Languages'" />
      <ProgrammingLanguages v-if="skillSelection == 'Programming languages'" />
      <SoftSkills v-if="skillSelection == 'Soft skills'" />
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import LanguagesSection from '../skillSections/LanguagesSection.vue'
import SoftSkills from '../skillSections/SoftSkills.vue'
import ToolsSection from '../skillSections/ToolsSection.vue'
import WebDevSection from '../skillSections/WebDevSection.vue'
import SkillsNavbar from '../SkillsNavbar.vue'
import ProgrammingLanguages from '../skillSections/ProgrammingLanguages.vue'

const skillSelection = ref<string | null>(null)

const handleSkillset = (skillset: string) => {
  skillSelection.value = skillset
}
</script>

<style scoped></style>
