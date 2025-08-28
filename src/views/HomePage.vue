<template>
  <div>
    <h1 class="text-center mx-auto my-8 text-xl md:text-2xl 2xl:text-3xl font-bold">
      <i class="fa-solid fa-at"></i>Lorenzo-Fenderico
    </h1>
    <NavBar />
    <h1
      class="text-7xl md:text-8xl 2xl:text-9xl mr-[10%] ml-[5%] xl:mr-[30%] my-[5%] font-bold flex justify-center"
    >
      Breach & Build
    </h1>
    <p
      class="text-[80%] md:text-[85%] lg:text-[120%] text-left ml-[25%] mr-[10%] md:ml-[30%] xl:ml-[40%]"
    >
      Hello! It's me Lorenzo, a self-taught penetration tester and developer. I love breaking into
      networks and building beautiful web experiences. Whether I'm hunting for vulnerabilities or
      crafting the perfect user interface, I'm always learning something new. Security and code are
      my passions—and I'm here to share what I've discovered along the way.
    </p>

    <img
      src="@/assets/photo/myself.webp"
      class="rounded-full size-75 md:size-100 2xl:size-120 object-cover mx-auto my-[5%]"
    />
  </div>

  <AboutSection />
  <SkillsSection />
  <ProjectsSection />
  <BlogSection />
</template>

<script setup lang="ts">
import NavBar from '@/components/NavBar.vue'
import AboutSection from '@/components/Sections/AboutSection.vue'
import BlogSection from '@/components/Sections/BlogSection.vue'
import ProjectsSection from '@/components/Sections/ProjectsSection.vue'
import SkillsSection from '@/components/Sections/SkillsSection.vue'
</script>

<style scoped></style>
