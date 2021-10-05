<template>
    <main>
        <Films v-for="(film, index) in allFilms" :key="index" :movie="film" />
    </main>
</template>

<script>
import Films from './Films.vue';

export default {
    name: 'Main',
    components: {
        Films
    },
    props: ['allFilms'],
}

</script>

<style>

</style>