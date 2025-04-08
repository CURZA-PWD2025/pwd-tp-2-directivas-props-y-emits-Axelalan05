<template>
  <h1>Peliculas</h1>
  <div class="container">
    <CardComponent v-for="peli in listaPeliculas" :key="peli.id" :movie="peli" @update_likes="sumarLike" />
  </div>
</template>

<script setup lang="ts">
import peliculas from './resource/movies.ts';
import { ref } from 'vue';
import type { Pelicula } from './interfaces/Pelicula.ts';
import CardComponent from './components/CardComponent.vue';
const listaPeliculas = ref<Pelicula[]>(peliculas);

const sumarLike = (id: number) => {
  const peli = listaPeliculas.value.find(p => p.id === id);
  if (peli) peli.likes++;
};
</script>

<style scoped>
.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1rem;
}
</style>
