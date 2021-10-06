<template>
    <div>
        <h3>{{tv.name}}</h3>
        <h5>{{tv.original_title}}</h5>
        <div class="lang"><lang-flag :iso="tv.original_language" :squared="false"/></div>
        <div class="vote">{{tv.vote_average}}</div>
    </div>
</template>

<script>
import LangFlag from 'vue-lang-code-flags';

export default {
    name: 'Tvs',
    props: ['tv'],
    components: {
        LangFlag,
    },
}
</script>

<style>

</style>