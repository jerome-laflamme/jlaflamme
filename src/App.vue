<script setup>
import YellowSection from "./components/YellowSection.vue";
import HeaderSection from "./components/HeaderSection.vue";
</script>

<template>
  <header>
    <HeaderSection />
  </header>

  <main>
    <YellowSection />
  </main>
</template>

<style scoped>
header {
  position: relative;
  width: 100vw;
  overflow: hidden;
}

header::before {
  content: "";
  display: block;
  padding-bottom: calc(100% * (1642 / 1102));
  background: url(./assets/img/background-image.jpg) no-repeat center center;
  background-size: cover;
}
</style>
