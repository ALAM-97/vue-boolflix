<template>
  <div id="app">
    <Header @search="searchFilms" />
    <Main :info="input"/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main
  },
  data() {
    return {
      input: "",
    }
  },
  methods: {
    searchFilms(userInput) {
      this.input = userInput;
    }
  }
}
</script>

<style lang="scss">
// #app {

// }
</style>
