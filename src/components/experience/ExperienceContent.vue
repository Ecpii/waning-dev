<script setup>
import TextBlock from '../TextBlock.vue';

</script>

<template>
  <article>
    <TextBlock>
      <header class="text-header">
        <b><a href="https://ramp.com" target="_blank" style="color: inherit">Ramp</a></b>
        <span class="date">Summer 2025</span>
      </header>
      <summary class="subtitle">Software Engineer Intern - Frontend</summary>

      <p>
        Super excited and grateful to work at Ramp in NYC this summer!!!!
      </p>
    </TextBlock>
    <TextBlock>
      <header class="text-header">
        <b>University of Michigan</b>
        <span class="date">Winter 2025</span>
      </header>
      <summary class="subtitle">Instructional Aide (EECS 479: Quantum Computing)</summary>

      <p>
        My first IA position, where I helped teach a class of 100 students about quantum computing fundamentals.
        Held a recorded lab section, office hours, and built a <a href="https://blochm.waning.dev/" target="_blank">
          3D visualization tool for it!</a>
      </p>
      <br />

      <p>
        Grateful to have taught this course the first semester it's an official class and hoping to return
        to continue and develop it!
      </p>
    </TextBlock>
    <TextBlock>
      <header class="text-header">
        <b>Tour.video (YC S21)</b>
        <span class="date">Summer 2023</span>
      </header>
      <summary class="subtitle">Full Stack Engineering Intern</summary>

      My first internship, where I learned a lot about what I did and didn't know about React and full-stack
      development!
      Specifically, the technologies I worked with were React, Flask, Supabase, BigQuery, Figma, novu, and 100ms.
      Engineered a lot of dashboards, notification systems, and forms, learning how to design as well from the team.
    </TextBlock>
  </article>
</template>
<style scoped>
.text-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

.date {
  color: var(--moon);
  font-size: 16px;
}

.entry-container {
  display: flex;
  width: 100%;
  gap: 20px;
  align-items: flex-start;
}

.image-container {
  width: 64px;
  height: 64px;
  padding: 4px;
  border-radius: 100%;
  background: var(--moon);
  flex: 0 0 auto;
  overflow: hidden;
}

.entry-container img {
  width: 56px;
  height: 56px;
  object-fit: contain;
}

.text-container {
  flex-grow: 1;
}

.subtitle {
  opacity: 0.8;
}
</style>
