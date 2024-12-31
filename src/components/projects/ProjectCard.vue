<script setup>
const props = defineProps(['data'])
</script>

<template>
  <div class="container">
    <div class="img-container">
      <img :src="`/projects/${props.data.image}`" :alt="`${props.data.name} thumbnail`" />
    </div>
    <div class="text-container">
      <h3>{{ props.data.name }}</h3>
      <span class="subtitle">{{ props.data.subtitle }}</span>
      <div class="tags">
        <span class="tag" v-for="tag in props.data.tags" :key="tag">{{ tag }}</span>
      </div>
      <div class="buttons">
        <a :href="props.data.mainButton.link" class="main-button" target="_blank" v-if="props.data.mainButton">
          {{ props.data.mainButton.text }}
        </a>
        <a :href="props.data.secondaryButton.link" class="secondary-button" target="_blank"
          v-if="props.data.secondaryButton">
          {{ props.data.secondaryButton.text }}
        </a>
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
  gap: 1rem;
  transition: 0.4s
}

.container:hover {
  background: var(--light-secondary)
}

@media (width < 740px) {
  .img-container {
    display: none;
  }

  .container {
    padding: 0 1rem;
    height: auto;
  }
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
  flex-wrap: wrap;
  color: var(--moon);
}

.buttons {
  display: flex;
  flex-wrap: wrap;
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

.img-container {
  height: 100%;
  width: 220px;
  clip-path: circle(120px at 85px 50%);
}

img {
  height: 100%;
  float: right
}
</style>
