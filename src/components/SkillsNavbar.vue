<template>
  <div>
    <div class="flex flex-row gap-8 min-w-max p-2 pt-0 text-sm lg:text-lg">
      <button
        @click="((skillset = 'Tools'), sendSkillsetInfo())"
        class="px-6 py-2 rounded-xl"
        :class="{ 'bg-black text-white': skillset == 'Tools' || null }"
      >
        Tools
      </button>
      <button
        @click="((skillset = 'Web development'), sendSkillsetInfo())"
        class="rounded-xl px-6 py-2"
        :class="{ 'bg-black text-white': skillset == 'Web development' }"
      >
        Web development
      </button>
      <button
        @click="((skillset = 'Programming languages'), sendSkillsetInfo())"
        class="rounded-xl px-6 py-2"
        :class="{ 'bg-black text-white': skillset == 'Programming languages' }"
      >
        Programming languages
      </button>
      <button
        @click="((skillset = 'Languages'), sendSkillsetInfo())"
        class="rounded-xl px-6 py-2"
        :class="{ 'bg-black text-white': skillset == 'Languages' }"
      >
        Languages
      </button>
      <button
        @click="((skillset = 'Soft skills'), sendSkillsetInfo())"
        class="rounded-xl px-6 py-2"
        :class="{ 'bg-black text-white': skillset == 'Soft skills' }"
      >
        Soft skills
      </button>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const skillset = ref<string | null>(null)

const emit = defineEmits(['skillset'])

const sendSkillsetInfo = () => {
  emit('skillset', skillset.value)
}
</script>

<style scoped></style>
