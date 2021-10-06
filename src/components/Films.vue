<template>
    <div>
        <img :src="`https://image.tmdb.org/t/p/w200/`+ movie.poster_path">
        <h3>{{movie.title}}</h3>
        <h5>{{movie.original_title}}</h5>
        <div class="lang"><lang-flag :iso="movie.original_language" :squared="false"/></div>
        <div class="vote">{{movie.vote_average}}</div>
    </div>
</template>

<script>
import LangFlag from 'vue-lang-code-flags';

export default {
    name: 'Films',
    props: ['movie'],
    components: {
        LangFlag,
    },
}
</script>

<style>

</style>