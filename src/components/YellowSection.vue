<script setup>
import { library } from "@fortawesome/fontawesome-svg-core";
import {
  faPhone,
  faEnvelope,
  faCode,
  faGripVertical,
} from "@fortawesome/free-solid-svg-icons";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";

library.add(faCode);
library.add(faGripVertical);
library.add(faPhone);
library.add(faEnvelope);
</script>

<template>
  <div id="yellow-section">
    <div class="left">
      <div class="rounded-picture">
        <img src="../assets/img/me.jpg" alt="Me" />
      </div>
      <div class="contact">
        <div class="inline">
          <font-awesome-icon icon="phone" />
          <p>514 884-9516</p>
        </div>
        <div class="inline">
          <font-awesome-icon icon="envelope" />
          <p>jerome@jlaflamme.com</p>
        </div>
        <div class="inline">
          <font-awesome-icon icon="code" />
          <p>github.com/jerome-laflamme</p>
        </div>
        <div class="inline">
          <font-awesome-icon icon="grip-vertical" />
          <p>croustine.xyz</p>
        </div>
      </div>
    </div>
    <div class="right">
      <div class="profile-content">
        <h2>Profil</h2>
        <div class="line" />
        <p>
          Développeur full-stack de formation, je me passionne pour l’art et le
          design.
        </p>
        <p>
          J’aime toucher à plusieurs domaines tels que la musique, la photo, les
          arts visuels, la modélisation 3D, le UI/UX Design, et le motion
          design. Je porte un grand intérêt aux nouvelles technologies et j'ai
          une soif de les apprendre. Les défis sont de mises pour me garder
          stimulé et intéressé.
        </p>
        <p>
          Expérience : JS, TS, React, Vue, CSS, HMTL, Three.JS, C#, MySQL,
          MongoDB, Node.JS, Blender, Figma, Photoshop, Illustrator, After
          Effects, Premiere Pro
        </p>
        <div class="color-palette">
          <div class="dark-blue"></div>
          <div class="light-blue"></div>
          <div class="red"></div>
          <div class="white"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
#yellow-section {
  display: flex;
  background-color: var(--yellow);
  height: 100vh;
  padding: 5% 15%;
  align-items: center;
}

.left {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  height: 100%;
  width: 30%;
}

.rounded-picture {
  width: 400px;
  height: 400px;
  border-radius: 50%;
  overflow: hidden;
}

img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.contact {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin-top: 10rem;
}

.inline {
  display: flex;
  align-items: center;
}

.contact p {
  margin: 10px;
  font-size: 1.2rem;
}

.right {
  width: 50%;
  padding-left: 10rem;
  display: flex;
  align-items: center;
  height: 100%;
}

.profile-content {
  height: 40%;
}

.profile-content h2 {
  font-size: 2rem;
  margin-bottom: 2rem;
}

.line {
  width: 70%;
  height: 3px;
  background-color: var(--grey);
  margin-bottom: 2rem;
  transform: translateX(-100px);
}

.profile-content p {
  font-size: 1.5rem;
  margin-bottom: 1.2rem;
}

.color-palette {
  display: flex;
  justify-content: flex-end;
  width: 100%;
  margin-top: 5rem;
}

.color-palette div {
  width: 60px;
  height: 40px;
}

.dark-blue {
  background-color: var(--dark-blue);
}

.light-blue {
  background-color: var(--light-blue);
}

.red {
  background-color: var(--red);
}

.white {
  background-color: var(--white);
}
</style>
