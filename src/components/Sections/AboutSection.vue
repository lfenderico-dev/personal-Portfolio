<template>
  <div class="h-fit flex flex-col gap-12 my-[10%] mx-[10%] lg:mx-[5%] lg:my-[15%]">
    <div class="flex flex-row items-center gap-4">
      <hr class="border-1 rounded-full inline w-[20%] bg-black" />
      <h1
        class="text-xl sm:text-2xl md:text-3xl lg:text-4xl xl:text-5xl 2xl:text-6xl text-center font-bold w-fit inline"
      >
        What sets me apart?
      </h1>
    </div>

    <div class="flex flex-col lg:flex-row gap-12 lg:gap-6 xl:gap-14">
      <img
        src="@/assets/photo/myself.webp"
        class="h-[50vh] w-[100%] sm:w-[80%] md:h-[65vh] sm 2xl:h-[95vh] mx-auto object-cover rounded-4xl shadow-2xl shadow-black"
      />
      <div
        class="flex flex-col text-center lg:text-left gap-6 text-lg xl:text-xl 2xl:text-2xl 2xl:gap-14 w-fit lg:justify-center"
      >
        <p>
          I’m a penetration tester with a strong focus on Wi-Fi security, also experienced in web
          app testing, OSINT, and frontend development. I approach security with an attacker’s
          mindset and a developer’s understanding—uncovering vulnerabilities others miss and
          translating them into actionable, code-aware fixes.
        </p>

        <p>
          Wireless networks are often overlooked, yet critical. I specialize in exposing real-world
          risks in this space, helping companies secure a key part of their infrastructure.
        </p>

        <p>
          I’m committed to continuous learning and staying ahead of evolving threats—constantly
          refining my tools, techniques, and knowledge to provide the highest value in every
          engagement.
        </p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped></style>
