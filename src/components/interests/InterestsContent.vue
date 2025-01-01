<script setup>
import TextBlock from '../TextBlock.vue';

let timeoutId;

async function setClipboard(text) {
  const type = "text/plain";
  const blob = new Blob([text], { type });
  const data = [new ClipboardItem({ [type]: blob })];
  await navigator.clipboard.write(data);
}

function handleDiscordCopy(event) {
  setClipboard("ecpi")
  console.log("ecpi")
  const targetElement = event.srcElement;
  console.log('event', event)
  console.log('targetElement', targetElement)
  targetElement.innerHTML = "username copied!"
  clearTimeout(timeoutId);
  timeoutId = setTimeout(() => targetElement.innerHTML = "Discord", 1000);
}
</script>

<template>
  <article>

    <TextBlock>
      <h3>Tetris/Stacker games</h3>
      <p>
        I love playing competitive modern stacker games. If you also do, don't hesitate to contact me on <a
          @click="handleDiscordCopy">Discord</a> to talk
        or play! If you don't, I have plenty of clips for you to watch!
      </p>
      <TextBlock><a href="https://four.lol/openers/hachispin" target="_blank">hachispin</a> is cool: <br />
        <iframe width="560" height="315" src="https://www.youtube.com/embed/G6bqbjiWp38?si=PCB1MZyRY2Bs1db6"
          title="YouTube video player" frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
      </TextBlock>
      <TextBlock>
        <a href="https://bit.ly/STStacking" target="_blank">ST Stacking</a> is cool: <br />
        <iframe width="560" height="315" src="https://www.youtube.com/embed/pzV6JPdtNcs?si=kkJrCTMzB-EWkQ8r"
          title="YouTube video player" frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
      </TextBlock>
      <TextBlock>
        get lucky: <br />
        <iframe width="560" height="315" src="https://www.youtube.com/embed/1IirWrOgIBU?si=exwZS0tly2uhNGt5"
          title="YouTube video player" frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
      </TextBlock>
    </TextBlock>
    <TextBlock>
      <h3>Cardistry</h3>
      <p>
        I had a really bad phase of impulsively buying a bunch of playing card decks when I’m in high school, and ended
        up
        picking up cardistry to start using them! If you're in the area, come to a Michigan Magic meeting sometime!
      </p>
      <br />
      <img src="/interests/cardistry.avif" alt="picture of all my irresponsible deck purchases" width="100%" />
    </TextBlock>
  </article>
</template>

<style scoped>
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
