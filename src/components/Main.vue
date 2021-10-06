<template>
    <main>
        <div class="films">
            <ul>
                <li v-for="(film, index) in allFilms" :key="index" >
                    <Films :movie="film" />
                </li>
            </ul>
        </div>
        <div class="series">
            <ul>
                <li v-for="(serie, index) in allSeries" :key="index" >
                    <TvSeries :tv="serie" />
                </li>
            </ul>
        </div>
    </main>
</template>

<script>
import Films from './Films.vue';
import TvSeries from './TvSeries.vue;';

export default {
    name: 'Main',
    components: {
        Films,
        TvSeries
    },
    props: ['allFilms','allSeries'],
}

</script>

<style>

</style>