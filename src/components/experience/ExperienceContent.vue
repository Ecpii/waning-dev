<script setup></script>

<template>
  <div class="entry-container">
    <div class="image-container">
      <img src="/src/assets/experience/tour.png" />
    </div>
    <div class="text-container">
      <div class="text-header">
        <h3>Tour.video</h3>
        <span class="date">Summer 2023</span>
      </div>
      <div class="subtitle">Full Stack Engineering Intern</div>
      <p>
        Tour.video is a YC startup that embeds interactive virtual tours on leasing websites,
        allowing properties to garner new leads automatically.
      </p>
      <br />
      <p>
        As an intern in this startup environment, I was able to get a lot of experience following
        features through from idea to deployment and make many critical design decisions myself.
      </p>
      <br />
      <p>
        Specifically, I built multiple notification pipelines to interact with visitors and boost
        engagement for clients’ websites, as well as a dashboard system to track and follow up with
        leads quickly.
      </p>
    </div>
  </div>
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
p {
  font-size: 16px;
}
</style>
