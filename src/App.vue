<template>
  <div id="app">
    <Header @search="searchFilms" />
    <Main :allFilms="films"/>
  </div>
</template>

<script>
import axios from 'axios';
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
      films: [],
      input: "",
    }
  },
  methods: {
  searchFilms(userInput) {
    this.input = userInput;
    axios.get('https://api.themoviedb.org/3/search/movie', {
          params: {
            api_key: 'cdcfe1113982652506af0e8193d0dd64',
            query: this.input ,
            language: 'it-IT'
          }
        })
        .then( (resp) => {
          this.films = resp.data.results;
          console.log(this.input)
          console.log(this.films)
        })
    }
  }
}
</script>

<style lang="scss">
// #app {

// }
</style>
