<template>
    <main>
        <ul>
            <li v-for="(film, index) in allFilms" :key="index" >
                <Films :movie="film" />
            </li>
        </ul>
        
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