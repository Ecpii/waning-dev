<script setup>
import Moon from './assets/moon.svg'
import GitHub from './assets/github.svg'
import LinkedIn from './assets/linkedin.svg'
import Document from './assets/document.svg'
import ProjectContent from './components/projects/ProjectContent.vue'
import PassionContent from './components/passion/PassionContent.vue'

import { ref } from 'vue'
import EducationContent from './components/education/EducationContent.vue'
import ExperienceContent from './components/experience/ExperienceContent.vue'

const page = ref(window.location.hash?.substring(1) ?? "projects");

function handleSectionClick(section) {
  page.value = section
}

const PAGES = [
  {
    text: "Projects",
    slug: "projects"
  },
  {
    text: "Experience",
    slug: "experience"
  },
  {
    text: "Education",
    slug: "education"
  },
  {
    text: "Interests",
    slug: "interests"
  },
]
</script>

<template>
  <div class="main-container">

    <header>
      <Moon />
      <div class="social-icons">
        <a href="https://github.com/Ecpii" target="_blank" aria-label="GitHub">
          <GitHub height="100%" width="100%" />
        </a>
        <a href="https://linkedin.com/in/wayne-he-" target="_blank" aria-label="Linkedin">
          <LinkedIn height="100%" width="100%" />
        </a>
        <a href="/resume.pdf" target="_blank" aria-label="Resume">
          <Document height="100%" width="100%" />
        </a>
      </div>
    </header>

    <main>
      <h1>Hello!</h1>
      <p>
        I'm <b>Wayne</b> <span class="light">(also sometimes known as <b>waning</b> or <b>ecpi</b>)</span>,
        and I make things with code. Mainly, my experience is in web development, but I'm very interested in operating
        systems, quantum computing, and programming languages!
      </p>
      <p>
        Currently, I'm studying my BSE in Computer Science at the University of Michigan. Outside of school, I enjoy
        learning about cardistry, stacker games, and East Asian languages.
      </p>

      <nav>
        <a @click="() => handleSectionClick(p.slug)" :class="`section-button ${page == p.slug && 'selected'}`"
          :href="`#${p.slug}`" v-for="p in PAGES" :key="p.slug">
          {{ p.text }}
        </a>
      </nav>
      <ProjectContent v-if="page == 'projects'" />
      <EducationContent v-if="page == 'education'" />
      <ExperienceContent v-if="page == 'experience'" />
      <PassionContent v-if="page == 'interests'" />
    </main>
  </div>
</template>

<style scoped>
.slide {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
}

header {
  margin-top: 32px;
  display: flex;
  gap: 2rem;
  flex-direction: column;
  /* position: sticky;
  top: 32px; */
}

nav {
  display: flex;
  justify-content: space-between;
  width: 100%
}

.section-button {
  font-size: 28px;
  font-weight: light;
  color: var(--text);
}

.selected {
  font-weight: bold;
  /* color: var(--moon) */
}

header>svg {
  filter: drop-shadow(0px 0px 6px var(--moon));
}

main {
  width: min(720px, calc(100vw - 2rem));
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.light {
  font-weight: 300;
}

.social-icons {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  align-items: center;
}

.social-icons a {
  width: 2.5rem;
  height: 2.5rem;
  color: var(--moon);
  filter: brightness(90%);
}

.social-icons a:hover {
  filter: brightness(120%);
  background: transparent;
}

.main-container {
  display: flex;
  gap: 1rem;
  max-width: max(50vw, 960px);
  margin: 162px 0;
}
</style>
