<script setup>
import ProjectCard from './ProjectCard.vue'
import projectData from './data.json'
</script>
<template>
  <article class="cards-container">
    <ProjectCard v-for="project in projectData" :key="project.name" :data="project" />
  </article>
</template>

<style scoped>
.cards-container {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
</style>
