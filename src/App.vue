
<script setup lang="ts">

// Importiert unsere selbst erstellte Komponente.
import ExerciseList from './components/ExerciseList.vue'

</script>

<template>
  <main class="app">

    <h1>FitTrack</h1>

    <p>Dein persönlicher Fitness-Tracker</p>

    <!-- Hier wird unsere Komponente angezeigt. -->
    <ExerciseList />

  </main>
</template>

<style scoped>
.app {
  max-width: 800px;
  margin: 40px auto;
  padding: 24px;
}

h1 {
  color: #42b883;
  font-size: 36px;
}

p {
  color: #777;
}
</style>
