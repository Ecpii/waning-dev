<script setup>
import Moon from './assets/moon.svg'
import GitHub from './assets/github.svg'
import LinkedIn from './assets/linkedin.svg'
import Document from './assets/document.svg'
import ProjectContent from './components/projects/ProjectContent.vue'
import InterestsContent from './components/interests/InterestsContent.vue'
import EducationContent from './components/education/EducationContent.vue'
import ExperienceContent from './components/experience/ExperienceContent.vue'

import { ref } from 'vue'
import { Analytics } from '@vercel/analytics/vue'

const PAGES = {
  "projects": {
    text: "Projects",
    slug: "projects",
    component: ProjectContent,
  },
  "experience": {
    text: "Experience",
    slug: "experience",
    component: ExperienceContent,
  },
  "education": {
    text: "Education",
    slug: "education",
    component: EducationContent
  },
  "interests": {
    text: "Interests",
    slug: "interests",
    component: InterestsContent
  },
}

const page = ref((window.location.hash?.substring(1) ?? "projects") || "projects");

function handleSectionClick(section) {
  page.value = section
}

</script>

<template>
  <Analytics />
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
        and I make things with code. Mainly, my experience is in web development, but I'm also interested in
        quantum computing, operating systems, and programming languages!
      </p>
      <p>
        Currently, I'm studying my BSE in Computer Science at the University of Michigan. Outside of school, I enjoy
        learning about cardistry, stacker games, and East Asian languages.
      </p>

      <nav>
        <a @click="() => handleSectionClick(key)" :class="`section-button ${page == key && 'selected'}`"
          :href="`#${p.slug}`" v-for="(p, key) in PAGES" :key="key">
          {{ p.text }}
        </a>
      </nav>
      <KeepAlive>
        <Transition name="slide-fade" mode="out-in">
          <component :is="PAGES[page].component" v-if="page" />
        </Transition>
      </KeepAlive>
    </main>
  </div>
</template>

<style>
.slide-fade-enter-active,
.slide-fade-leave-active {
  z-index: -1;
  transition: all 0.2s;
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateY(40px);
  opacity: 0;
}
</style>

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
  flex-wrap: wrap;
  width: 100%;
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
  width: 100%;
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
  width: 90vw;
  max-width: 840px;
  margin: 162px 0;
}

@media (width < 740px) {
  .main-container {
    flex-direction: column;
    margin: 2rem 0;
  }

  header {
    align-items: center;
  }

  .social-icons {
    flex-direction: row
  }

  nav {
    flex-direction: column;
    align-items: stretch;
  }

  nav>a {
    text-align: center
  }
}
</style>
