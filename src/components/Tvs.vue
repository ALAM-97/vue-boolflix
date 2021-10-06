<template>
    <div>
        <img :src="`https://image.tmdb.org/t/p/w200/`+ tv.poster_path">
        <h3>{{tv.name}}</h3>
        <h5>{{tv.original_title}}</h5>
        <div class="lang"><lang-flag :iso="tv.original_language" :squared="false"/></div>
        <div class="vote">{{starVote()}}</div>
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
    data() {
        return {
            roundedNum: ""
        }
    },
    methods: {
        starVote() {
            const halfNum = this.tv.vote_average / 2;
            this.roundedNum = Math.ceil(halfNum);
            return this.roundedNum;
        }
    }
}
</script>


<style lang="scss" scoped>
    @import '../assets/style/common.scss';

</style>