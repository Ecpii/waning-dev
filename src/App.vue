<script setup>
import GithubIcon from './assets/github-mark.svg'
</script>

<template>
  <header>header</header>

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
      learning about cardistry, stacker games, anime, and Asian languages.
    </p>

    <div class="social-icons">
      <a href="https://github.com/Ecpii" target="_blank">
        <GithubIcon width="100%" height="100%" />
      </a>
    </div>
    <h2>Projects</h2>
  </main>
</template>

<style scoped>
main {
  position: absolute;
  top: 200px;
  left: 50%;
  transform: translateX(-50%);
  background: var(--secondary);
  border-radius: 20px;
  padding: 1rem 2rem;
  width: 720px;
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
