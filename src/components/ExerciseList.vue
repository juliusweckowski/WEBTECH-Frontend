
<script setup lang="ts">

// Beschreibt den Aufbau einer Übung.
// Jede Übung benötigt eine ID, einen Namen
// und eine Kategorie.
interface Exercise {
  id: number
  name: string
  category: string
}

// Unsere Liste mit drei Beispielübungen.
// Später sollen diese Daten aus dem Backend kommen.
const exercises: Exercise[] = [
  {
    id: 1,
    name: 'Bankdrücken',
    category: 'Kraft'
  },
  {
    id: 2,
    name: 'Joggen',
    category: 'Cardio'
  },
  {
    id: 3,
    name: 'Plank',
    category: 'Isometric Hold'
  }
]

</script>

<template>
  <section class="exercise-list">

    <h2>Meine Übungen</h2>

    <!-- v-for durchläuft alle Übungen in der Liste -->
    <ul>
      <li
        v-for="exercise in exercises"
        :key="exercise.id"
      >
        <strong>{{ exercise.name }}</strong>
        <span>{{ exercise.category }}</span>
      </li>
    </ul>

  </section>
</template>

<style scoped>
.exercise-list {
  margin-top: 30px;
}

h2 {
  margin-bottom: 20px;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 18px;
  margin-bottom: 12px;
  background-color: #eef5f1;
  border-radius: 10px;
  color: #1b3026;
}

span {
  color: #476456;
}
</style>
