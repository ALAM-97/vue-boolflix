<template>
    <div>
        <img :src="`https://image.tmdb.org/t/p/w200/`+ movie.poster_path">
        <h3>{{movie.title}}</h3>
        <h5>{{movie.original_title}}</h5>
        <div class="lang"><lang-flag :iso="movie.original_language" :squared="false"/></div>
        <div class="vote" v-for="(star, index) in starVote()" :key="index"><i class="fas fa-star"></i></div>
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
    data() {
        return {
            roundedNum: ""
        }
    },
    methods: {
        starVote() {
            const halfNum = this.movie.vote_average / 2;
            this.roundedNum = Math.ceil(halfNum);
            return this.roundedNum;
        },
        stars() {
            for (let i = 0; i <= this.roundedNum; i++) {
                return `<i class="fas fa-star"></i>`
            }
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/common.scss';

</style>