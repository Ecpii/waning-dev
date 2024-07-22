<script setup>
import ProjectCard from './ProjectCard.vue'
import projectData from './data.json'
</script>
<template>
  <ProjectCard v-for="project in projectData" :key="project.name" :data="project" />
</template>
