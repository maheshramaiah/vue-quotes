<template>
  <div id="app">
    <Banner :count="quotes.length"></Banner>
    <AddQuote :addQuote="addQuote" :disable="quotes.length === maxQuote"></AddQuote>
    <QuoteList :quotes="quotes" :deleteQuote="deleteQuote"></QuoteList>
  </div>
</template>

<script>
import Banner from './components/Banner.vue'
import AddQuote from './components/AddQuote.vue'
import QuoteList from './components/QuoteList.vue'

export default {
  components: {
    Banner,
    AddQuote,
    QuoteList
  },
  data () {
    return {
      maxQuote: 10,
      quotes: []
    }
  },
  methods: {
    addQuote (quote) {
      this.quotes.push(quote)
    },
    deleteQuote (index) {
      this.quotes = this.quotes.filter((q, i) => i !== index)
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
