<script setup>
import Moon from './assets/moon.svg'
import GitHub from './assets/github.svg'
import LinkedIn from './assets/linkedin.svg'
import Document from './assets/document.svg'
import ProjectContent from './components/projects/ProjectContent.vue'
import PassionContent from './components/passion/PassionContent.vue'
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
      I'm <b>waning</b> <span class="light">(also sometimes known as <b>ecpi</b>)</span>, and I make
      things with code. I also enjoy playing puzzle games and learning about cardistry.
    </p>
    <p>
      Currently, I'm studying Computer Science at the University of Michigan. I've done a decent amount of work in web
      development here, but I'm also very interested in dev tools, new languages, and quantum programming!
    </p>

        <div class="slide">
          <h2>Projects</h2>
          <ProjectContent />
        </div>
        <!-- <div class="slide">
          <h2>Passions</h2>
          <PassionContent />
        </div> -->
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
}

header > svg {
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
  margin-top: 162px;
}
</style>
