<script setup></script>

<template>
  <div>
    <div class="title">
      <h3>University of Michigan</h3>
      <span class="date">Aug 2022 - May 2026</span>
    </div>
    <p>
      Majoring in Computer Science at the College of Engineering with a minor in Electrical
      Engineering. Some of my favorite courses here:
    </p>
    <div class="bullets">
      <ul>
        <li>Web Systems (EECS 485)</li>
        <div class="indent">
          building dynamic web applications and search engines using Flask + React
        </div>
        <li>Quantum Computing (EECS 498)</li>
        <div class="indent">
          building quantum algorithms using unitary gates and limited resources!
        </div>
        <li>Intro to Computer Security (EECS 388)</li>
        <div class="indent">
          building and breaking web, crypto, and application (binary) level security protocols
        </div>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.title {
  display: flex;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}
li::marker {
  color: var(--moon);
  filter: drop-shadow(0px 0px 8px var(--moon));
}
.date {
  color: var(--moon);
  font-size: 16px;
}
.bullets {
  width: 100%;
}
.indent {
  margin-left: 2rem;
  font-style: italic;
}
</style>
