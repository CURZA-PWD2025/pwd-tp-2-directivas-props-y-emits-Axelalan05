<template>
    <div class="card">
        <img :src="movie.portada" :alt="movie.titulo" />
        <h2>{{ movie.titulo }}</h2>
        <p><strong>Año:</strong> {{ movie.anio }}</p>
        <p><strong>Director:</strong> {{ movie.director }}</p>
        <p><strong>Generos:</strong> {{ movie.generos.join(', ') }}</p>
        <button @click="likeMovie">❤️ {{ movie.likes }}</button>
    </div>
</template>

<script setup lang="ts">

import { defineProps, defineEmits } from 'vue';
import type { Pelicula } from '../interfaces/Pelicula.ts';

const props = defineProps<{
    movie: Pelicula
}>();

const emit = defineEmits<{
    (e: 'update_likes', id: number): void
}>();

const likeMovie = () => {
    emit('update_likes', props.movie.id)
};

</script>

<style scoped>
.card {
    border: 1px solid #ccc;
    padding: 1rem;
    margin: 1rem;
    border-radius: 10px;
    width: 300px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

img {
    width: 100%;
    border-radius: 5px;
}
</style>