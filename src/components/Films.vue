<template>
    <div>
        {{movie.title}}
        {{movie.original_language}}
        {{movie.vote_average}}
    </div>
</template>

<script>
export default {
name: 'Films',
props: ['movie']

}
</script>

<style>

</style>