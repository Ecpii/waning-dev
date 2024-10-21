<script setup>
import Moon from './assets/moon.svg'
import GitHub from './assets/github.svg'
import LinkedIn from './assets/linkedin.svg'
import Document from './assets/document.svg'
import ProjectContent from './components/projects/ProjectContent.vue'
import PassionContent from './components/passion/PassionContent.vue'
import { Splide, SplideSlide } from '@splidejs/vue-splide'
import '@splidejs/vue-splide/css'
</script>

<template>
  <header>
    <Moon />
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
    <Splide :options="{
      width: '100%',
      pagination: false,
      autoHeight: true,
      rewind: true,
      gap: '2rem',
      speed: 600,
    }">
      <SplideSlide>
        <div class="slide">
          <h2>Projects</h2>
          <ProjectContent />
        </div>
      </SplideSlide>
      <SplideSlide>
        <div class="slide">
          <h2>Passions</h2>
          <PassionContent />
        </div>
      </SplideSlide>
    </Splide>
  </main>
</template>

<style>
.splide__arrow {
  top: 0.5rem;
  transform: none;
  background: url('./assets/moon-button.svg');
  background-size: contain;
  background-repeat: no-repeat;
  opacity: 0.8;
}

.splide__arrow:hover:not(:disabled) {
  opacity: 1;
}

.splide__arrow--next {
  transform: rotate(180deg);
}

.splide__arrow svg {
  display: none;
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
  position: absolute;
  top: 20px;
  left: 50%;
  transform: translateX(-50%);
  filter: drop-shadow(0px 0px 6px var(--moon));
}

main {
  position: absolute;
  top: 200px;
  left: 50%;
  transform: translateX(-50%);
  background: var(--primary);
  border-radius: 20px;
  padding: 1rem 2rem;
  width: min(720px, calc(100vw - 2rem));
  display: flex;
  align-items: center;
  flex-direction: column;
  gap: 1rem;
}

.light {
  font-weight: 300;
}

.social-icons {
  display: grid;
  gap: 0.75rem;
  place-items: center;
  grid-template-rows: 1.75rem;
  grid-auto-columns: 1.75rem;
  grid-auto-flow: column;
}

.social-icons a {
  color: var(--text);
  filter: brightness(90%);
}

.social-icons a:hover {
  filter: brightness(120%);
  background: transparent;
}
</style>
