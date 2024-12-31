<template>
  <section>
    <slot></slot>
  </section>
</template>

<style scoped>
section {
  padding: 0.5rem;
  transition: 0.4s;
}

section:hover {
  background-color: #353e6580;
}
</style>