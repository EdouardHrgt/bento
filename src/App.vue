<script setup>
import Create from './components/Create.vue'
import Write from './components/Write.vue'
import Social from './components/Social.vue'
import Manage from './components/Manage.vue'
import Maintain from './components/Maintain.vue'
import Schedule from './components/Schedule.vue'
import Grow from './components/Grow.vue'
import Faster from './components/Faster.vue'
</script>

<template>
  <div class="wrap">
    <main class="container">
      <Social />
      <Manage />
      <Maintain />
      <Schedule />
      <Grow />
      <Faster />
      <Create />
      <Write />
    </main>
  </div>
</template>

<style scoped>
.wrap {
  min-height: 100vh;
  display: grid;
  place-items: center;
}

.container {
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  grid-auto-rows: 200px;
  gap: 16px;
  max-width: 1500px;
  margin-inline: auto;
  align-items: stretch;
}

/* 1. Social (grand bloc au centre) */
.container > *:nth-child(1) {
  grid-column: 2 / 4;
  grid-row: 1 / 2;
}

/* 2. Manage */
.container > *:nth-child(2) {
  grid-column: 2 / 3;
  grid-row: 2 / 3;
}

/* 3. Maintain */
.container > *:nth-child(3) {
  grid-column: 3 / 4;
  grid-row: 2 / 3;
}

/* 4. Schedule (colonne droite, grand) */
.container > *:nth-child(4) {
  grid-column: 4 / 5;
  grid-row: 1 / 3;
}

/* 5. Grow (bas droite large) */
.container > *:nth-child(5) {
  grid-column: 3 / 5;
  grid-row: 3 / 4;
}

/* 6. Faster (centre bas) */
.container > *:nth-child(6) {
  grid-column: 2 / 3;
  grid-row: 3 / 4;
}

/* 7. Create (gauche haut) */
.container > *:nth-child(7) {
  grid-column: 1 / 2;
  grid-row: 1 / 2;
}

/* 8. Write (gauche bas, grand) */
.container > *:nth-child(8) {
  grid-column: 1 / 2;
  grid-row: 2 / 4;
}

@media (max-width: 900px) {
  .wrap {
    min-height: auto;
    display: block;
  }
  .container {
    padding-inline: 1rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 2rem;
    padding-block: 2rem;
  }
}
</style>
