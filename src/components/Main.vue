<template>
    <main>
        <Films/>
    </main>
</template>

<script>
import axios from 'axios';
import Films from './Films.vue';

export default {
    name: 'Main',
    components: {
        Films
    },
    props: ['info'],
    data() {
        return {
            foundFilms: [],
        }
    },
    created() {
        axios
            .get('https://api.themoviedb.org/3/search/movie', {
                params: {
                    api_key: 'cdcfe1113982652506af0e8193d0dd64',
                    query: 'ritorno dal futuro', //da importare dalla search,
                    language: 'it-IT'
                }
            })
    }
}

</script>

<style>

</style>