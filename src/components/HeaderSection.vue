<script setup>
import { library } from "@fortawesome/fontawesome-svg-core";
import { faArrow } from "@fortawesome/free-solid-svg-icons";
import { onMounted, ref } from "vue";

library.add(faArrow);

const containerRefs = ref([]);

onMounted(() => {
  containerRefs.value.forEach((content) => {
    let totalWidth = 0;

    content.childNodes.forEach((node) => {
      if (node.clientWidth) {
        totalWidth += node.clientWidth + 40; // 40px is the sum of the left and right margins
      }
    });

    content.style.width = `\${totalWidth}px`;
  });
});

const headerIsMoving = ref(false);
</script>

<template>
  <div class="yellow-container">
    <div v-if="headerIsMoving">
      <div
        :key="container"
        ref="container => containerRefs.value.push(container)"
        class="container-content"
      >
        <h1>JEROME</h1>
        <h1>LAFLAMME</h1>
        <div class="dot-icon">
          <svg
            width="15"
            height="15"
            viewBox="0 0 100 100"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <circle cx="50" cy="50" r="50" fill="var(--grey)" />
          </svg>
        </div>
        <h1>portfolio</h1>
      </div>
    </div>

    <div v-else class="fixed-title">
      <h1>JEROME LAFLAMME</h1>
      <h2>portfolio</h2>
    </div>
  </div>
  <div class="controls">
    <div class="arrow-icon">
      <font-awesome-icon
        icon="arrow"
        @click="headerIsMoving = !headerIsMoving"
      />
    </div>
  </div>
</template>

<style scoped>
.yellow-container {
  display: flex;
  align-items: center;
  justify-content: center;
  position: fixed;
  background-color: var(--yellow);
  width: 700px;
  height: fit-content;
  z-index: 1;
  top: 10%;
  right: 0;
  overflow: hidden;
}

.container-content {
  display: flex;
  justify-content: center;
  align-items: center;
  animation: slide 7s linear infinite;
}

.container-content > * {
  margin: 0 20px;
}

h1 {
  font-size: 5rem;
}

.fixed-title {
  text-align: right;
  position: fixed;
  background-color: var(--yellow);
  width: 1300px;
  height: 250px;
  padding: 50px 200px;
  z-index: 1;
  top: 10%;
  right: 0;
  overflow: hidden;
}

.arrow-icon {
  position: fixed;
  top: 50%;
  right: 0;
  transform: translateY(-50%);
  z-index: 1;
  cursor: pointer;
  color: var(--yellow);
}
@keyframes slide {
  0% {
    transform: translateX(100%);
  }
  100% {
    transform: translateX(-100%);
  }
}
</style>
