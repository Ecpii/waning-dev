<script setup></script>

<template>
  <div>
    <h3 class="title">Tetris/Stacker games</h3>
    <p>
      I love playing competitive modern stacker games. If you also do, don't hesitate to contact me on Discord to talk
      or play! If you don't, I have plenty of clips for you to watch!
    </p>
    <div class="bullets">
      <ul>
        <li><b><a href="https://four.lol/openers/hachispin">hachispin</a></b> is my favorite opener...</li>
        <iframe width="560" height="315" src="https://www.youtube.com/embed/G6bqbjiWp38?si=PCB1MZyRY2Bs1db6"
          title="YouTube video player" frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
        <div class="caption">
          ... though it might not be optimal
        </div>
        <li>You should learn <a href="https://bit.ly/STStacking">ST Stacking</a>...</li>
        <iframe width="560" height="315" src="https://www.youtube.com/embed/pzV6JPdtNcs?si=kkJrCTMzB-EWkQ8r"
          title="YouTube video player" frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
        <div class="caption">
          ... though it's less suited for multiplayer compared to LST
        </div>
        <li>play in whatever way makes you happy!</li>
        <iframe width="560" height="315" src="https://www.youtube.com/embed/1IirWrOgIBU?si=exwZS0tly2uhNGt5"
          title="YouTube video player" frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
        <div class="caption">
          even if that means opener maining!
        </div>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.title {
  text-align: center;
}

ul {
  padding-right: 40px;
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

.caption {
  text-align: center;
  font-style: italic;
  margin-bottom: 1rem;
}
</style>
