<template>
    <main>
        <div class="films">
            <h2>FILMS</h2>
            <ul>
                <li v-for="(film, index) in allFilms" :key="index" >
                    <Films :movie="film" />
                </li>
            </ul>
        </div>
        <div class="tvs">
            <h2>TV SERIES</h2>
            <ul>
                <li v-for="(serie, index) in allSeries" :key="index" >
                    <Tvs :tv="serie" />
                </li>
            </ul>
        </div>
    </main>
</template>

<script>
import Films from './Films.vue';
import Tvs from '../components/Tvs.vue';

export default {
    name: 'Main',
    components: {
        Films,
        Tvs
    },
    props: ['allFilms','allSeries'],
}

</script>

<style>

</style>