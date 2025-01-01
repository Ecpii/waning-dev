<script setup>
import TextBlock from '../TextBlock.vue';

</script>

<template>
  <article>
    <TextBlock>
      <header class="text-header">
        <b>University of Michigan</b>
        <span class="date">Winter 2025</span>
      </header>
      <summary class="subtitle">Instructional Aide (EECS 479: Quantum Computing)</summary>

      <p>
        This semester, I am very fortunate to be an IA for the newly official Quantum Computing class at UMich! If you
        haven’t already, take a look at the qubit visualization project I made for this class after I took it!
      </p>
      <br />

      <p>
        This class covers a lot of really cool and increasingly relevant stuff like Steane/Shor’s error correcting
        codes,
        Grover’s Algorithm, Shor’s Algorithm, QFTs and more so I’m excited to teach it! I’ll be teaching a weekly lab
        section, holding office hours, and helping students online, as well as maintaining Bloch M.
      </p>
      <br />
      <p>
        If you’re in this class and on this page, that’s cool! Feel free to ask me about anything in class or outside!
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
