<template>
    <header>
        <form>
            <input v-model="userInput" type="text" >
            <button @click.prevent="$emit('search', userInput)">Cerca</button>
        </form>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            userInput: ''
        }
    }
}
</script>

<style lang="scss" scoped>

</style>