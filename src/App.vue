<script setup>
import Moon from './assets/moon.svg'
import GithubIcon from './assets/github-mark.svg'
import ProjectCard from './components/ProjectCard.vue'
import projectCardInfo from './projectCardInfo.json'
</script>

<template>
  <header>
    <Moon />
  </header>

  <main>
    <h1>Hello!</h1>
    <p>
      I'm <b>waning</b> <span class="light">(also sometimes known as <b>ecpi</b>)</span>, and I make
      things with code. I'm a fan of all things tech, but I'm currently very interested in quantum
      computing and secure programming.
    </p>
    <p>
      Currently, I'm studying my BSE in Computer Science at the University of Michigan (Ann Arbor),
      where I'm also the president of
      <a href="https://maizepages.umich.edu/organization/tetris">Michigan Tetris</a>. I enjoy
      playing puzzle games, learning cardistry, watching anime, and eating pineapple on pizza.
    </p>

    <div class="social-icons">
      <a href="https://github.com/Ecpii" target="_blank">
        <GithubIcon width="100%" height="100%" />
      </a>
    </div>
    <h2>Projects</h2>
    <ProjectCard v-for="cardInfo in projectCardInfo" :key="cardInfo.name" :data="cardInfo" />
  </main>
</template>

<style scoped>
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
  gap: 0.5rem;
  place-items: center;
  grid-template-rows: 2rem;
  grid-auto-columns: 2rem;
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
