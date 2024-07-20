<script setup></script>

<template>
  <div class="container">
    <img src="../assets/blochm.png" alt="bloch m" />
    <div class="text-container">
      <h3>Bloch M</h3>
      <span class="subtitle">A tool for visualizing all single-qubit gates and states.</span>
      <div class="tags">
        <span class="tag">Vue</span>
        <span class="tag">Three.js</span>
        <span class="tag">Lorem</span>
      </div>
      <div class="buttons">
        <a href="" class="main-button"> Homepage </a>
        <a href="" class="secondary-button"> Repository </a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  border-radius: 20px;
  background: var(--secondary);
  width: 100%;
  height: 156px;
  overflow: hidden;
  display: flex;
}
.text-container {
  padding: 0.75rem 0;
  display: flex;
  flex-direction: column;
}
.subtitle {
  opacity: 0.8;
}
.tags {
  margin-top: 0.25rem;
  display: flex;
  gap: 1rem;
  font-size: 16px;
  color: var(--moon);
}
.buttons {
  display: flex;
  gap: 1rem;
  margin-top: 1rem;
  font-size: 16px;
}
.buttons a:hover {
  filter: brightness(110%);
}
.main-button {
  background: var(--accent);
  color: var(--text);
  border-radius: 20px;
  padding: 0.125rem 1rem;
  font-weight: 500;
}
.secondary-button {
  color: var(--text);
  font-weight: 500;
  padding: 0.125rem 0;
}
img {
  height: 100%;
  clip-path: circle(110px at 75px 75px);
}
</style>
